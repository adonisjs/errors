# E_CANNOT_SWAP_SERVER

### Why This Error Occurred
This error occurs when you are trying to update the underlying HTTP server reference after it has been started. So always make sure `Server.setInstance` is called before `Server.listen`.

### Possible Ways to Fix It
- You will not face this issue when using AdonisJs default blueprints. In case you are using a different blueprint, make sure to contact the package author.