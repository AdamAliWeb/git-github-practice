# Git & Github Practice

This repo serve as visible practice for mastering the use of Git and Github. Maybe I could have several of this practice repositories

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
