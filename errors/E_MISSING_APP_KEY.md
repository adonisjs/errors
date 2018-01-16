# E_MISSING_APP_KEY

### Why This Error Occurred
This exception is raised when `appKey` is missing inside `config/app.js` file. The config file references the value of `APP_KEY` from `.env` file.

### Possible Ways to Fix It
- Make sure `.env` file exists and `APP_KEY` is defined inside it.
- Make sure the config file is referencing the right key.
- Run `adonis key:generate` to re-generate the APP_KEY and save it inside the `.env` file.