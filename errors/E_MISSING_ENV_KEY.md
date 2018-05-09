# E_MISSING_ENV_KEY

### Why This Error Occurred
This exception is raised when an environment variable is missing in `process.env`.

### Possible Ways to Fix It
- Make sure `.env` file exists and environment variable is defined inside it.
- Set environment variable from the command line, before running the command, e.g. `FOO=1 npm start`

### See Also
 - [AdonisJS docs](https://adonisjs.com/docs/4.1/configuration-and-env) for environment variable configuration
 - [Node.js docs for `process.env`](https://nodejs.org/api/process.html#process_process_env)
 - [Docs for `dotenv` package](https://www.npmjs.com/package/dotenv) that is used internally by AdonisJS to load environment variables from `.env` file.
