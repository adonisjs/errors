# E_MISSING_CONFIG

### Why This Error Occurred
This exception is raised when any one of the module is unable to find the required configuration from the `config` directory of your application.

It can be due to a missing config file or badly configured config file.

### Possible Ways to Fix It
- Each official package of AdonisJs, includes a sample config file within the same repo under the `config` directory. For example: The config file for `@adonisjs/auth` is saved inside [config/index.js](https://github.com/adonisjs/adonis-auth/config/index.js) file, so make sure to reference this file.
