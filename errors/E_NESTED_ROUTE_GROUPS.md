# E_NESTED_ROUTE_GROUPS

### Why This Error Occurred
This error occurs when you are trying to create nested Route groups. Nested route groups are not allowed for the sake of simplicitly.

**Note** it is fine to grow the routes file in the number of lines, but not in complexity.

### Possible Ways to Fix It
- Do not call `Route.group` one inside the another.
- Use the following technique to apply shared properties on a group.

```js
const addPrefixToGroup = (group) => {
  group.prefix('api/v1')
  return group
}

addPrefixToGroup(Route.group(() => {
  Route.get('users', () => {})
}))
```

Now any group, that is passed to `addPrefixToGroup` method will get a prefix. This way you are not nesting groups and also writing shared code at a single place.