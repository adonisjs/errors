# E_INVALID_MIDDLEWARE_TYPE

### Why This Error Occurred
This error occurs when you are trying to bind a middleware which is not a `function` and neither a `string`.

**Note**: AdonisJs only allows following styles of middleware.

1. Reference to IoC container binding.

```js
'App/Middleware/Acl'
```

2. A plain function.

```js
Route
.get()
.middleware([
  function () {
  }
])
```

### Possible Ways to Fix It
- Make sure you are not binding a reference to some kind of an `object` or `undefined/null` values.
