In this implementation of an external service, the code is written for NodeJS and the Express framework is used. Several Node packages are used to handle the routine tasks of REST request processing to process the Inline Hook calls that come from Okta.


```javascript
const express = require('express');
const basicAuth = require('express-basic-auth')
const { body, validationResult } = require('express-validator');
const bodyParser = require('body-parser');
```

We're also going to separate out into its own file the code that implements the business logic of this external service, which is the actual check of the submitted user credentials against our user store:

```javascript
const users = require('./users');
```
