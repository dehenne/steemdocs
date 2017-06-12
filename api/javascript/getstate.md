# getState

Returns the posts for a given tag/category.

**Arguments**

`name` String - Path for the category. \('created', 'created/steem'\)

```
steem.api.getState(path, function(err, result) {
  console.log(err, result);
});
```



