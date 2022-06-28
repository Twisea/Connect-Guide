# Making a Post
This section will guide you through making a post for your Connect account.

## The `post` command
There is only one way to make a post with Connect, and that is with the `/post` command.

`/post <option: [Text | Image | Poll]>`
:   The `post` command will show an embed with three buttons and a select menu.

    === "`Content` Button"
        The `Content` button will display a form for you to put your post content. There will always be a `title` field that is optional, but, depending on your post type, there will either be a `content` field or an `image URL` field. These secondary fields are required.
    
    === "`Create` and `Cancel` Buttons"
        The `create` button will create your post, but is disabled until your post has either content or an image URL. The `cancel` button will cancel your post.
    
    === "`Extra Options` Select Menu"
        The `Extra Options` select menu will display a list of options for you to choose from. These include marking your post as NSFW or selecting whether to make the post also available on your linked Twitter account. 
    
    The `post` command takes three options:

    `Text`
    :   A `text` post is a post consisting of two text fields. The title is optional and can have as much as fifty characters, while the content is required and can have up to 300 characters.

    `Image`
    :   An `image` post is a post consisting of a title and an image. The title is optional and can have up to fifty characters, while the image URL is required and can have up to 200 characters.

    `Poll`
    :   A `poll` post is a post consisting of a title and a poll. The title is optional and can have up to fifty characters, while the poll is required and can have from 2-4 options.

    !!! tip "Extra Fields"
        The `color` field is another field used to customize the color of your post's embed. This field is only available with Connect Plus.

## Information About Connect Post Creation
While most of the post creation process is decided by you, the user, there's a few checks and processes that go on behind the scenes.

=== "NSFW Image Detection"
    Thanks to a handy [NSFW image detection API](https://deepai.org/machine-learning-model/nsfw-detector) provided by [DeepAI](https://deepai.org), Connect will automatically detect if your post is NSFW. If it decides that your image is, in fact, NSFW, it will automatically mark your post as NSFW. You will not be able to change this unless you change the image in your post to something non-NSFW.

=== "Post Filtering"
    If you've already taken a look at the [your account](/your-account) page, you'll see that you can filter the posts that you see based on toxicity and profanity. Once you hit that handy `create` button, Connect will pass your post title and content through a handy AI Model and decide a toxicity ranking from 0-2. `0` means your post is completely clean, and `2` means that your post is very toxic. Users cannot view what toxicity ranking is on their post.

!!! tip "The Art of Connect Post Creation"
    Titles aren't required, but are good for reeling a user in before you go into the content of your post. Try making a title something that a user would be interested in reading more of. As for the content, try to keep it interesting or funny. Nobody wants to see spam and nonsense. In fact, spam may have a chance of getting removed from the platform.