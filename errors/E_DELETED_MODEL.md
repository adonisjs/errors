# E_DELETED_MODEL

### Why This Error Occurred
This error occurs when you are trying to modify an instance of deleted row. For example:

```js
const user = await User.find(1)
await user.delete()

user.email = 'foo@bar.com'
```

Above code will throw this exception

### Possible Ways to Fix It
- Simply do not edit the model instance after deletion.