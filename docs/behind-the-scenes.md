# Behind the Scenes

This file goes over a few functions and systems that go on behind-the-scenes. You may not know they exist, but their crucial for your experience with Connect and sometimes how it works.

## Connect Standard Post Navigator (CSPN)

Connect Standard Post Navigator, or CSPN, is the paginator and UI that you see when looking through posts. Every single time you see a post, it's made possible by CSPN. It can handle anywhere from loads and loads of posts to only one or two. It's what makes the whole Connect experience possible and is probably the most important part of the bot. Without it, you wouldn't be able to see *any* posts. We spent the most time by far reconfiguring, rewriting, and coding CSPN so it can make your Connect experience special.

### How it Works

!!! warning "Nerd Stuff Ahead"

    If you don't know anything about "Python," "subclassing," or programming in general, you probably won't find the following information useful, nor will you know what any of it means.

CSPN is made possible by our amazing programming skills (of course) and Pycord's `pages` extension. There are three parts to CSPN:

- The Paginator

- CSPN's view

- Posts

=== "The Paginator"
    The Paginator is a big part of CSPN. It handles changing posts and timeouts. It's also responsible for telling the view what to do and when. It also has most of the important attributes and properties, such as who's viewing the posts and a list of the posts. The paginator is subclassed from Pycord's `ext.pages` Paginator, and that makes it a lot easier to control and handle.

=== "The View"
    The view is one of the biggest parts of CSPN. It's responsible for displaying, updating, and using the buttons attached to it. Each button has its own method responsible for doing what it's told, and the view is a big container responsible for holding them all and making sure they don't run away. Without it, you wouldn't be able to do anything to posts.

=== "The Posts"
    Before showing you the posts, we have to pass them through a post-to-pageinator. This makes all of our posts easily digestible for the paginator, which will probably throw a fit if we feed it pure, organic posts instead of processed posts. These handle what happens when a post gets viewed, as well as making it easier for the paginator to use.

## Content Moderation

There are multiple moderation features in place so users don't post anything bad. While most content is allowed in Connect, it still has to be filtered and categorized so people can avoid it at will. There are multiple things moderating posts:

### NSFW Detection

Using a handy NSFW detection API, we can safely determine whether an uploaded image is NSFW or not. So if some rapscallion decides to upload an NSFW image and *not* mark it as NSFW, our handy dandy NSFW detector will find out and label your post appropriately. 

This API is free to use and made by DeepAI. The API can be found [here](https://deepai.org/machine-learning-model/nsfw-detector).

### AI-Powered Post Filtering

When anything gets posted, any words, texts, or links get passed through an AI-Powered post filtering machine. This has three ratings ranging from 0-2. 0 means the post is clean and has no bad words and phrases in it, while 2 is very bad and contains toxicity, profanity, and very mean posts. 

Both guilds and users can configure their own preferred filter, so you only see posts with that specific filter or lower. So if you set your preferred filter level to 2, which is the default, you'll see all Connect posts. If you set it to 0, you'll only see the cleanest and nicest posts on Connect. Guild-set filters take priority, so if a guild has their preferred filter level set at 0 and you have yours set at 2, Connect will take the guild's level and filter by that. However, if a guild filter is larger than your own, your filter is the one that takes the cake. So if a guild has a preferred filter level of 1 and you have yours 0, posts will be filtered by 0. 

Keep in mind that NSFW posts will always be only available in age-restricted channels, regardless of filter levels.