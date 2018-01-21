# E_MISSING_DATABASE_ROW

### Why This Error Occurred
This error occurs when you call any `orFail` method, trying to look up a record in database.

```js
const user = await User.findOrFail(1)
```

Above code will throw this exception, when a user with `id=1` doesn't exists.

### Possible Ways to Fix It
- Wrap your `orFail` calls inside a try/catch block.
```js
try {
  const user = await User.findOrFail(1)
} catch (error) {
 // handle error
}
```
- Or do not use `orFail` method.
```js
const user = await User.find(1)
if (!user) {
}
```
