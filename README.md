# Git & Github Practice

This repo serve as visible practice for mastering the use of Git and Github. Maybe I could have several of this practice repositories

I can create a github repository in the website and then just clone in my PC to start working

## SSH Keys

To establish a connection in my PC through the new SSH Keys method and be able to push to my repositories more comfortable, I have to follow these steps:

```bash
ssh-keygen -t ed25519 -C "emailAddress@gmail.com"
```

You can change the location of the keys and add a password. Each time you try to establish a connection you have to write that password. But you can just skip that part hitting enter.

Then you have to add the key to your github profile. Enter to `settings -> SSH and GPG Keys` and then create a new key. You have to paste the key content in order to add the key, to do that smoothly there is a command you can use to have it already on the clipboard

```bash
clip < ~/.ssh/id_ed25519.pub
```

For the last step to test and establish the connection you have enter this command. If it ask you to establish connection type `yes`

```bash
ssh -T git@github.com
```

And that's it. You can push to any of your repositories, make sure to push through the SSH method.

## Tips

> > > When pulling from a repository it's better to use `git pull --rebase`. This instead of merging the commits you put the new commits in you local work

> > > While merging or rebasing, If you made a mistake you can go back adding `--abort` after git merge/rebase.

> > > To be able to check the commits which weren't pushed, use `git log --oneline --branches --not --remotes`

> > > To go back to a previous commit it depends if the commit was pushed to the repo. If no then use `git reset "commit"`. If yes then use `git revert`
