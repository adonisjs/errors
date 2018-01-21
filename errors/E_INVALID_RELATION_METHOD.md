# E_INVALID_RELATION_METHOD

### Why This Error Occurred
This error occurs when you are trying to invoke a method on a relationship, but that relationship does not support that operation.

For example: The `belongsTo` relation doesn't have `save` method. Instead you all `associate`.

### Possible Ways to Fix It
- Go through the documentation and make sure you are not invoking unsupported relationship methods.