# comment()

Submits a post or comment to the blockchain.

## Arguments

`WIF` - The WIF key for the autor

`parentAuthor` - Only if its a comment, the name of the post author.

`parentPermlink` - If comment. For a post use main category.

`author` - Author of the post/comment. You.

`title` - Title if post.

`body` - Body of post/comment. Markdown or HTML.

`json_metadata` - JSON object with meta data like tags, images, format and app.

`callback` - Callback function for error/result handling.


## Example
Submit a post.

       steem.broadcast.comment(
          // WIF
          this.props.wif,
          // parentAuthor
          "", // none for a new post
          // parentPermlink or main category
          h.createTagArray(post.tags)[0],
          // 'steem-dev',
          // author
          this.props.user,
          // permlink
          h.createPermLink(post.title),
          // ["steem-dev", "steem", "steemit", "dev", "tools"],
          // title
          post.title,
          // body
          post.body,
          // json_metadata
          JSON.stringify({
            tags: h.createTagArray(post.tags),
            app: "insteem/0.1",
            format: "markdown",
            community: "insteem"
          }),


