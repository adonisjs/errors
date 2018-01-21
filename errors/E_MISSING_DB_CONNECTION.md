# E_MISSING_DB_CONNECTION

### Why This Error Occurred
This error occurs when database you are trying to use has not been defined inside `config/database.js` file.

### Possible Ways to Fix It
- Make sure to define the connection inside `config/database.js` file. Check [example config file](https://github.com/adonisjs/adonis-lucid/master/blob/config/index.js) for reference.
