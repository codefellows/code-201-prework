## Install VSCode Text Editor

Now it's time to install VSCode Text Editor, a sophisticated text editor for code, markup, and prose.

To get started, download [VSCode](https://code.visualstudio.com/download), and after it is installed, launch the application.

[VSCode's documentation](https://code.visualstudio.com/docs) is excellent. Review it now to familiarize yourself with the basics.

### Install shell commands

You'll find it useful to open files and directories in VSCode from the terminal, but that functionality needs to be configured first. 

Open the **Command Palette** (⇧⌘P) and type 'shell command' to find the **Shell Command: Install 'code' command in PATH** command.

Restart the terminal for the new $PATH value to take effect. You'll be able to type 'code .' in any folder to start editing files in that folder. If VSCode opens, you're good to go.

If VSCode does not open, try the above process again. If it still does not work, we will remedy it during lab on the first day of class.

### Associate VSCode with Git

It's important to establish a default editor with Git (version control software) so that when Git opens files, that happens in your chosen editor.

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

#### Verify the Node installation

Now let's verify that it is installed. Enter the following into your terminal:

`nodejs -e 'console.log("works")'`

You should get a response that says "works". If not, try reinstalling Node again. If you are still having issues, please contact your instructor.

### Install ESLint

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your terminal (Ubuntu on Windows) and enter:

`npm -g i eslint git-open`

You should see a lot of feedback as it installs.

### Verify the installation

Now let's verify that ESLint is installed. Enter the following into your terminal:

`npm list -g --depth=0`

You should see ESLint among the list of installed packages. If not, run the previous installation command again.

### What is this linter thing?

Linting is the process of running a program that will analyze code for potential errors, some of which are syntax errors and some of which are style errors. It is an important part of the quality assurance process.

> `lint` was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs) in C language source code. The term is now applied generically to tools that flag suspicious usage in software written in any computer language. [Wikipedia]

That means the linter is your friend! It will help you write syntactically correct code, so you can catch errors in your text editor, rather than having to navigate to the browser, refresh your page, and search for errors. Faster feedback makes for happier developers (that's you!).

### Integrate ESLint with VS Code

Download and install the ESLint extension for VS Code [here](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). In VS Code, click the gear icon in the lower left corner and select Command Palette. Search for an option named `ESLint: Enable ESlint` and click on it to enable linting within your editor. VS Code will now display errors and warnings in your JavaScript files.

### Git Prompt Setup

To get started, run the following command.

```
nano ~/.bash_profile
```
This will open the file in your command line editor Nano

Copy and paste this code into the editor, **underneath any existing content.**

```
#!/usr/bin/env bash
# get current branch in git repo
function parse_git_branch() {
	BRANCH=`git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/\1/'`
	if [ ! "${BRANCH}" == "" ]
	then
		STAT=`parse_git_dirty`
		echo "[${BRANCH}${STAT}]"
	else
		echo ""
	fi
}
# get current status of git repo
function parse_git_dirty {
	status=`git status 2>&1 | tee`
	dirty=`echo -n "${status}" 2> /dev/null | grep "modified:" &> /dev/null; echo "$?"`
	untracked=`echo -n "${status}" 2> /dev/null | grep "Untracked files" &> /dev/null; echo "$?"`
	ahead=`echo -n "${status}" 2> /dev/null | grep "Your branch is ahead of" &> /dev/null; echo "$?"`
	newfile=`echo -n "${status}" 2> /dev/null | grep "new file:" &> /dev/null; echo "$?"`
	renamed=`echo -n "${status}" 2> /dev/null | grep "renamed:" &> /dev/null; echo "$?"`
	deleted=`echo -n "${status}" 2> /dev/null | grep "deleted:" &> /dev/null; echo "$?"`
	bits=''
	if [ "${renamed}" == "0" ]; then
		bits=">${bits}"
	fi
	if [ "${ahead}" == "0" ]; then
		bits="*${bits}"
	fi
	if [ "${newfile}" == "0" ]; then
		bits="+${bits}"
	fi
	if [ "${untracked}" == "0" ]; then
		bits="?${bits}"
	fi
	if [ "${deleted}" == "0" ]; then
		bits="x${bits}"
	fi
	if [ "${dirty}" == "0" ]; then
		bits="!${bits}"
	fi
	if [ ! "${bits}" == "" ]; then
		echo " ${bits}"
	else
		echo ""
	fi
}

# PS1 is what actually defines what you command line prompt looks like.
export PS1="\[\e[31m\]\u\[\e[m\]\[\e[35m\]\w\[\e[m\]\[\e[33m\]\`parse_git_branch\`\[\e[m\]\[\e[32m\]\\$\[\e[m\] "
```
Press `control X` to exit

Type `y` to verify changes

Hit `enter` to exit Nano

Now close terminal and open a new terminal window for changes to take effect.
You will have a new prompt with additional Git and color-coded features.
Don't worry about what this means for now. You will come to understand it's value very soon if you don't already.

### [⇐ Previous](3_git.md) | [Back to README ⇒](../../../../)
