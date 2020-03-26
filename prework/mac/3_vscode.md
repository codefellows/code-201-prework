# Install VSCode Text Editor

Now it's time to install VSCode Text Editor, a sophisticated text editor for code, markup, and prose.

To get started, download [VSCode](https://code.visualstudio.com/download). **As you finish downloading, it is critical that you go through installation following these steps, in exactly this order:**

1. Download the .zip file.
2. Double-click the .zip file (or click the downloaded file at the bottom of Chrome) to extract the shiny VS Code app.
3. Drag the shiny VS Code app into your Applications folder.
4. Open the app. (If you opened the app before it was in your Applications folder, you'll need to reinstall.)
5. (optional) Add the app to the Dock.

[VSCode's documentation](https://code.visualstudio.com/docs) is excellent. Review it now to familiarize yourself with the basics.

## Install shell commands

Open VSCode

Open the **Command Palette** (⇧⌘P) and type 'shell command' 

Then, click on the **Shell Command: Install 'code' command in PATH** command.

Restart the terminal for the new $PATH value to take effect. 

## Associate VSCode with Git

It's important to establish a default editor with Git (version control software) so that when Git opens files, that happens in your chosen editor.

Type the following command in your terminal:
`git config --global core.editor "code --wait"`

This command will not return any message unless there is an error.

# Install Node

*Note*: If you get an error while installing these packages such as "try again as root/administrator", you may need to use the `sudo` command to get administrator access. For example `sudo apt-get install nodejs`. 

To install Node, open your Terminal, and enter:

`brew install node`

It will take a few minutes for the download and installation process to complete.

# Install ESLint

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your terminal and enter:

`npm -g i eslint git-open live-server`

You should see a lot of feedback as it installs.

### [⇐ Previous](2_homebrew.md) | [Next ⇒](4_git.md)
