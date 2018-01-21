# E_CANNOT_NEST_RELATION

### Why This Error Occurred
This error occurs when you are trying to get count of *nested relations* using `withCount` method. 

**Let's understand why it is not possible.**

In the following query we will fetch the posts count for a single user.

```js
await User.query().withCount('posts').first()
```

Output

```js
{
	id: 1
	username: '...',
	postsCount: 3
}
```

Now if you try to fetch `comments count` for the post using `withCount('posts.comments')`. Lucid has no place to store this value as `postsCount` is an integer and not an object.

### Possible Ways to Fix It
In this case, what you need is to fetch the user, with the posts and comments count for each post. So use the following approach

```js
await User.query().with('posts', (builder) => {
  builder.withCount('comments')
}).first()
```

Output

```js
{
	id: 1
	username: '...',
	posts: [
	  {
	  	id: 4,
	  	commentsCount: 10
	  }	
	]
}
```
