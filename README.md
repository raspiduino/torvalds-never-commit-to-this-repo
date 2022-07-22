# Torvalds never commited to this repo

But why Github shows that?

Github shows the committed user by looking at git's `user.email`. From [Github's docs](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/troubleshooting-commits/why-are-my-commits-linked-to-the-wrong-user):

> GitHub uses the email address in the commit header to link the commit to a GitHub user.

And from [this page](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-email-preferences/setting-your-commit-email-address):
> Note: If you created your account on GitHub.com **_after July 18, 2017_**, your noreply email address for GitHub is a seven-digit ID number and your username in the form of ID+username@users.noreply.github.com. If you created your account on GitHub.com **_prior to July 18, 2017_**, your noreply email address from GitHub is username@users.noreply.github.com. You can get an ID-based noreply email address for GitHub by selecting (or deselecting and reselecting) Keep my email address private in your email settings.

So, if user A created an account before July 18, 2017, then someone else (user B) use his `username@users.noreply.github.com` to set to `user.email` and get user A's name from Github Profile, when user B commits to his repo, the committer will be shown as user A, when user A have no idea about the commit.

I sent opened a bug report to Github, hopefully they will reply :)

Some people actually did this, probably to trick people :)
