# Install Homebrew

You may already have Homebrew installed. Let's see if you do. Type

```
which brew
```

If Homebrew *is* installed, you will see some text like `/usr/local/bin/brew` followed by the command prompt on the next line. 

If **not** installed, you will **not** get an error message or a message of any kind. 

Now it's time to install Homebrew, a package manager for OS X. If you've never heard of a package manager, think of it as an App Store of **free** command line programs.

NOTE: **If you do not have XCode installed**, be sure to agree when asked to install the XCode Command Line Tools, which is necessary for installing Homebrew. It will ask you for your password, and won't show you any feedback as you type it (not even "••••••"). This installation may take up to 30 minutes to download and install, depending upon your network connection speed.

To get started, run the following command.

```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/install/master/install)"
```

### Update Homebrew

If you've previously installed Homebrew, now's a good time to update it by running the following command.

```
brew update
```

**TIP:** Run this command periodically as Homebrew doesn't auto-update itself.


### Verify Homebrew

To verify Homebrew is installed correctly, run the following command.

```
brew doctor
```

If Homebrew is you'll see something like this:

`Your system is ready to brew`

If Homebrew is not installed, you will see something like:

`-bash: brew: command not found`

### Install Tree view

Now that we've verified that homebrew was installed, we can use it to install a useful command for us called tree!

Type `brew install tree` into the command line.

Onces that's complete, you should now be able to type tree and your terminal will display all of your directories and folders in an awesome looking tree view format!

### [⇐ Previous](1_terminal.md) | [Next ⇒](3_vscode.md)
