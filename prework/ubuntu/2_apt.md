# Update APT

Now that your Terminal is setup, it's time to update Ubuntu's **Advanced Packaging Tool** or <a href="https://help.ubuntu.com/lts/serverguide/apt-get.html" target="_blank">APT</a> for short. If you've never heard of a package manager, think of it as an App Store of **free** command line programs.

To get started, run the following commands. Each line is its own command, so copy, paste, and run them one at a time.

```
sudo add-apt-repository -y ppa:git-core/ppa
sudo apt-get update
```

**TIP:** This may require your account password which **will not** appear on the screen as you type, but is tracking your key-strokes.

## Install Tree view

Once that's done we can install a quick awesome command called `tree`. What `tree` does is displays all of your directories and files in a nicely formatted tree so you can easily see your current file structure!

Type `sudo apt install tree`. Once that's done, you can type `tree` to see the tree view of the directory that you're currently in! You may have to close and restart your terminal before it will work.

### [⇐ Previous](1_terminal.md) | [Next ⇒](3_git.md)
