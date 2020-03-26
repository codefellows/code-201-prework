# Updating your Terminal

This section will talk about how to update the Terminal's look and feel, as well as how to edit files in Ubuntu through it's command line editor nano.

At the end, this will add some color to your command line, and your command line will be formatted for development.

## Updating the .profile file

1. Open the Ubuntu app and type `ls -a`. You should see a .profile file there. 
	- **If not**, then type `sudo touch .profile`.
2. Type `sudo nano .profile`. This will open the file in the command line editor Nano.
3. Copy and paste this code into the editor below any existing text. **This can be tricky**
	- You can only paste with a single right-click:

```
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
export PS1="\[\e[m\]\[\e[36m\]\W\[\e[m\]\[\e[33m\]\`parse_git_branch\`\\$ "


# Everything above this point is used to change how your terminal looks. If you ever want to update your terminals look, change things above here.


# Nothing below here will change how your terminal looks, rather, it will change some things about how it works.

# This allows you to open html files in Chrome more easily by typing "chrome filename".	
alias chrome="/mnt/c/Program\ Files\ \(x86\)/Google/Chrome/Application/chrome.exe"	

# This allows you to switch between the Ubuntu root and your Windows Root.

# wr evaluates to the absolute path to your Windows user's root.
export wr=~/../../mnt/c/Users/WIN_USERNAME/

# This gives us a quick way of moving directly to the Windows root
alias cdwr='cd "$wr"'

# This brings you to your Windows Working directory immediatly when you open a new terminal.
cdwr

```

4. After pasting that in, you will need to replace `WIN_USERNAME` with your **Windows username**, right after `.../Users/`. IE: `/Users/MichaelLeonTreat/`.

    -NOTE: If your path or username has a space, you can use a backslash escape character to include the space. IE: `/Users/Michael\ Treat/`.
    
If you are unsure what your Windows username is, then search 'command prompt' in the start menu and open it.

Type the following command `echo %username%` .  The result should be your Windows username. Replace `WIN_USERNAME` with this.

Close the command prompt.

After that you're done in the nano editor, so press `ctrl + x`. 

Hit `y` and the editor will save your changes. 

Hit enter.

- To navigate to the Ubuntu root, you will type `cd ~` (There is a space between cd and ~)

Now type `pwd` . You should see something like `/home/ubuntuusername`

- To navigate to the Windows root, you will type `cdwr`

Now type `pwd` . You should see something like `/mnt/c/Users/windowsusername`

**From this point on every time you close and re-open your Ubuntu terminal you will be starting in your Windows root.  This is where you will be working**

### Install Tree view

Once that's done we can install a quick awesome command called `tree`. What `tree` does is displays all of your directories and files in a nicely formatted tree so you can easily see your current file structure!

Type `sudo apt install tree`. Once that's done, you can type `tree` to see the tree view of the directory that you're currently in! You may have to close and restart your terminal before it will work.

### [⇐ Previous](./02_WSL_Ubuntu_setup.md) | [Next ⇒](./05_VSCode_Node_GIt_install.md)
