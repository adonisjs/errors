# E_INCOMPLETE_CONFIG

### Why This Error Occurred
This exception is raised when config for a given module is in-complete. For example: The database configuration is missing the database name.

### Possible Ways to Fix It
- Each official package of AdonisJs, includes a sample config file within the same repo under the `config` directory. For example: The config file for `@adonisjs/auth` is saved inside [config/index.js](https://github.com/adonisjs/adonis-auth/config/index.js) file, so make sure to reference this file.
