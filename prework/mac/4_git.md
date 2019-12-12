### Install Git

Check if you already have <a href="http://git-scm.com/" target="_blank">Git</a> installed by running the following command.

```
git --version
```

You'll see something like this if it's installed. If it is, skip to Git Config, otherwise continue below.

![](https://i.imgur.com/jBSs1qR.png)

Figure out what version of OS X you are running. From the Apple menu, choose About This Mac. The version of OS X installed appears directly below “OS X.” Click the version number to see the build number. You can also use <a href="https://support.apple.com/en-us/HT203001" target="_blank">System Information</a> to find these numbers.

![](https://support.apple.com/library/content/dam/edam/applecare/images/en_US/osx/yos_build_version.png)

If you are running:

- 10.6 Snow Leopard: download and install this: <a href="http://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download" target="_blank">git-*-snow-leopard</a>

- 10.7 Lion: download and install this <a href="http://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download" target="_blank">git-*-snow-leopard</a>

- 10.8 Mountain Lion: download and install this <a href="http://sourceforge.net/projects/git-osx-installer/files/git-2.3.5-intel-universal-snow-leopard.dmg/download" target="_blank">git-*-snow-leopard</a>

- 10.9 Mavericks: download and install this <a href="http://sourceforge.net/projects/git-osx-installer/files/git-2.5.3-intel-universal-mavericks.dmg/download" target="_blank">git-*-mavericks</a>

- 10.10 Yosemite or higher: continue below

**NOTE:** You will need to change your install permissions to be able to install Git. The installer will prompt you to do so if necessary.

Using Homebrew, you can install Git, the version control system of choice among choosy developers.

Version control systems let programmers share and collaborate on code. With Git, multiple programmers can work on the same files, and Git keeps track of who made what changes, when. Git is usually used with a website, GitHub, that stores code (in "repositories") and lets programmers review and discuss changes before they are added. In short, Git makes everyone's lives easier.

To get started, run the following command.
```
brew install git
```

Once it is fully installed, run the following command.

```
git --version
```

And you'll see something like this.

![](https://i.imgur.com/jBSs1qR.png)

### Git Config

You're on the home stretch now! :racehorse:

Like artists, programmers sign their work. Let's configure Git to sign your commits with your name and email address.

Sign up for an account at Github <a href="https://github.com" target="_blank">here</a>.

**WARNING:** Before running the following commands, replace `YOUR FULL NAME` and `YOUR EMAIL ADDRESS` with the name and email from <a href="https://github.com/settings/profile" target="_blank">your GitHub account</a>.

```
git config --global user.name 'YOUR FULL NAME'
git config --global user.email 'YOUR EMAIL ADDRESS'
git config --global core.editor 'code --wait'
```

The terminal does not send success messages, in order to double check that you have successfully assigned your username and email:

```
git config --list
```

Your terminal should output the following lines, among others:

```
user.email='YOUR EMAIL ADDRESS'
user.name='YOUR FULL NAME'
core.editor='code --wait'
```
### Git Prompt Setup

To get started, run the following command.
```
nano ~/.bash_profile
```

This will open the file in your command line editor Nano

Copy and paste this code into the editor, **underneath anything else already in this file:**

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

Hit `return` to exit Nano

Now close terminal and open a new terminal window for changes to take effect.
You will have a new prompt with additional Git and color-coded features.
Don't worry about what this means for now. You will come to understand it's value very soon.

### Congratulations!

You have now completed Step 3 of 9 in the Code 201 pre-work. Please follow the README link below to complete the remaining steps (4-9).

### [⇐ Previous](3_vscode.md) | [Back to README ⇒](../../../../)
