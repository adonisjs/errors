# E_MISSING_NAMED_MIDDLEWARE

### Why This Error Occurred
This errors occurs when you are trying to use a middleware on `Route`, but never defined it inside `start/kernel.js` file.

### Possible Ways to Fix It
- Make sure to define the middleware under `named` object as shown below.

**start/kernel.js**
```js
const namedMiddleware = {
  auth: 'App/Middleware/Auth'
}
```

**start/routes.js**
```js
Route
.get()
.middleware(['auth'])
```