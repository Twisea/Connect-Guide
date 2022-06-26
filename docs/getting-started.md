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