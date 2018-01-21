# E_CANNOT_OVERRIDE_RELATION

### Why This Error Occurred
This error occurs when you are trying to eagerload a single relationship for multiple times. AdonisJs throws an exception, since you are wasting database resources.

**Following code snippet will this raise this exception.**
```js
const user = await User.find(1)

await user.load('posts')

// duplicate call
await user.load('posts')
```

### Possible Ways to Fix It
- Make sure you are not loading the same relationship for multiple times, especially look at loops closely.
- You can check the existence of relationship as shown below.
```js
if(!user.getRelated('posts')) {
  await user.load('posts')
}
```
- To re-fetch the posts from database, run following code.
```js
const posts = user.getRelated('posts')
for (let post of posts.rows) {
  await post.reload()
}
```