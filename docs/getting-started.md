# Getting Started with Connect

Welcome to Connect! If you're completely new, you can get started one of two ways:

1. Create an account with the `/account create` command
2. Simply start using the bot!

## Creating a Connect Account
Thanks to a new system, you no longer have to go through the account creation process to use the bot. Once you use a command that needs information, Connect automatically creates an account for you based on your Discord account information. While this may be handy to get quickly started with Connect, the `account create` command gives you more control over how your account looks right off the bat.

If you decide to use the `account create` command, there's a few options you can configure to make your account look awesome. These include:

- Username
- Display Name
- Gender
- Birthday

!!! info "The Tip of the Iceburg"
    That's just the top of the iceburg when it comes to customizing your Connect account. With the `account edit` command, you can customize so much more, including your avatar and language.

Take a look at the [your account](/your-account) page to learn more about what can be added to your account and what can be done with it.

## Viewing Posts
There are currently four feed commands to view posts:

`/feed`
:   The `feed` command will show you posts from the users you follow in order from latest to oldest.

`/latest`
:   The `latest` command will display the latest posts from everyone using Connect, regardless of whether you follow them.

`/explore`
:   The `explore` feed will show you random posts from everyone using Connect. This command could also be referred to as "shuffle."

`/trending`
:   The `trending` feed will show you posts from the past week sorted by amount of likes and comments in descending order.

??? "Connect Standard Post Navigation"
    Connect Standard Post Navigation, or "CSPN," is what Connect uses to navigate between posts. It's what you see whenever you look at a post, whether you're using a feed command or viewing a post on its own. It's made via a combination of Pycord's `ext.pages` and rigorous subclasssing.

## Viewing Users
Of course, you can also interact with other users. There are multiple commands for this:

`/view user <user: [Username]>`
:   The `view user` command will show you the profile of the user you specify. The command takes the user's username.

`/view posts <user: [Username]>`
:   The `view posts` command will show you the posts of the user you specify. The command takes the user's username.

You can also follow users. You can either use the `/follow` command or view the user's account with `/view user` and click the green `follow` button.

## Making Your First Post
Making a post with Connect is fairly easy. You need to use the `/post` command.

To learn about creating a post, check out the [Making a Post](/making-a-post) section.
    

