## Install VSCode Text Editor

Now it's time to install VSCode Text Editor, a sophisticated text editor for code, markup, and prose.

To get started, download [VSCode](https://code.visualstudio.com/download), and after it is installed, launch the application.

[VSCode's documentation](https://code.visualstudio.com/docs) is excellent. Review it now to familiarize yourself with the basics.

### Install shell commands

Open the **Command Palette** (⇧⌘P) and type 'shell command'

Then, click the **Shell Command: Install 'code' command in PATH** command.

Restart the terminal for the new $PATH value to take effect. 

### Associate VSCode with Git

Type the following command in your terminal:
`git config --global core.editor "code --wait"`

This command will not return any message unless there is an error.

### Install Node

To install Node, open your Terminal and copy and paste the following line, then hit Enter:

`sudo apt-get install nodejs`

Afterwards, you'll want to install Node Package Manager (NPM).

`sudo apt-get install npm`

If you run into issues trying to install Node from these steps, please contact your instructor.

It will take a few minutes for the download and installation process to complete.

### Install ESLint

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your terminal and enter:

`npm -g i eslint git-open`

You should see a lot of feedback as it installs.

# Final Steps

### VSCode Extensions

1. To add extensions to VSCode, open up VSCode. On the bottom left hand side you will see a cog icon.  Click this and select extensions. A side-bar will slide out and at the top you can search for the listed extensions below and click the green 'Install' button:

  - live server 5.6.1
  - ESLint 2.0.13
  - HTML Snippets 0.2.1
  - HTML Preview 0.2.5
  - Debugger for Chrome

### Verification

#### By the time you’ve completed the guide, you should be able to run the following commands in your terminal:

- code --version
- git --version
- node --version
- npm --version
- eslint --version
- tree --version
- echo $PS1
- cat ~/.gitconfig
- code
  - should open VScode

#### Each command should report a version number of what’s installed (should look *similar* to below example). Should you run across any errors that give you trouble please get a hold of contact below:

``` 
username@user $ code --version
1.40.2
f359dd69833dd8800b54d458f6d37ab7c78df520
x64
username@user $ git --version
git version 2.2.0
username@user $ node --version
v10.16.0
username@user $ npm --version
6.9.0
username@user $ eslint --version
v6.7.2
username@user $ tree --version
tree v1.8.0 (c) 1996 - 2018 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro
username@user $ echo $PS1
\[\e[36m\]\A\[\e[m\] \[\e[32m\]\w\[\e[m\] \[\e[37;40m\]`parse_git_branch`\[\e[m\]
username@user $ cat ~/.gitconfig
[core]
	editor = code --wait
[user]
	name = yourgithubusername
	email = youremail
username@user $ code
//should open VSCode
```
---

#### Need help or have questions about computer setup?

Please contact our Admissions Support Instructor: <brad.smialek@codefellows.com> 

## THE END! 

### [⇐ Previous](3_git.md) | [Back to README ⇒](../../../../)
