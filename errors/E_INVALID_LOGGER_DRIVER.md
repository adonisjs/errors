# E_INVALID_LOGGER_DRIVER

### Why This Error Occurred
When the logger driver you are trying to use is not registered with the Logger.

### Possible Ways to Fix It
- Make sure the driver name is defined inside the config file.
- If you are using a plugin that adds additional drivers, then make sure it does extends the `Logger` interface as follows.

```js
const { ioc } = require('@adonisjs/fold')
ioc.extend('Adonis/Src/Logger', 'driverName', function (app) {
  return new Driver()
})
```