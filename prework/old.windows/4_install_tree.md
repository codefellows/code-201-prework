# Install Tree view for Windows.

## Context:

Tree view allows you to list all directories, sub-directories, and files in a nicely formatted view inside your terminal.

### Windows:

For windows, there are two options to choose from. 

1. The default tree command.

By default, you can use the cmd that comes from windows, but the command is a little long, and the display for it doesn't look that nice.

2. The GnuWin Tree command.

Alternatively, you can download, install, and update your path to use a program called tree which looks a lot cleaner than the default tree.


#### Option 1: Default tree.

This is the basic tree view command that comes with Windows. It works great in windows, but it doesn't look that good inside of our git bash terminal. Only use this command if you don't go with option 2. If you do go with option two, then ignore this command altogether.

To display the default tree view, type: `cmd //c tree`. This command only shows the directories and subdirectories. If you want to see the files as well, then type `cmd //c tree //f`.



#### Option 2: Install GnuWin Tree view.


**Read through this entire walkthrough at least once before doing it! If you are confused about any steps then feel free to wait until class starts and have a TA walk through this with you :)**

For a nicer layout, you can follow these instructions to download and install a couple that will allow you to just type `tree` and it will display a nicely formatted layout.

##### Step 1: Download, install, and unzip the needed files.

- Navigate to this site: `http://gnuwin32.sourceforge.net/packages/tree.htm`.
- Next, download the Setup on the line that says:  `Complete package, except sources`. This will download a basic installer for Tree.
- Then, download the binaries zip folder. We need this to add the tree command to our Path.
- There is an image to help point them out [here](https://imgur.com/a/jcznS)
   
- Next, run the installer that you downloaded called `tree-1.5.2.2-setup.exe`. Just select all the default values when prompted. ( Note that the version number may be different.)
- Next, extract or 'unzip' the binaries folder. When it asks you where to extract it to, enter this: `C:/Program Files/Tree`.

##### Step 2: Add the Tree program to your Path.

At this point, you have now installed tree onto your computer, but you still cannot use the command because it's not added to your Path. 
If you were to try to type `tree` in git bash now you would see and error like `bash: tree command not found`. This is because git bash doesn't know where to look to find the program that we just installed. By adding it to our path, we will be giving our git bash a direct path to find our tree program.

- Open your system settings. ( On windows 10 you can right click on the start menu and navigate to settings ).

- You should see a search bar. Type `env` and the search will populate with a couple options. Choose the option that says "Edit the System Environment Settings".
![](https://i.imgur.com/ZT7xvD9.png)

- A small window will pop-up. At the bottom, directly above the cancel button, is another button that says Environment Variables. Click that.
![](https://i.imgur.com/IjkiSrk.png)

- Another window will pop-up. This is where you can see all of your environment variables. Click on the one that says PATH, and then click edit.
![](https://i.imgur.com/t25DE7n.png)

- Finally, this last page will show you all of the things that are attached to your PATH. If you have installed VS Code you may seem it in here! Click on New and you'll see a text entry box appear in the middle of the page. Copy this line: `C:/Program Files/Tree/bin` and paste it in that entry field. Hit enter and then make sure to click Okay on all 3 previous boxes!
![](https://i.imgur.com/1RmmVdh.png)

Now at this point when you type `tree` in git bash, git bash will look at your path, look in the bin folder, and will find the tree program and will execute it. If it doesn't work then restart your computer and try again.


If it doesn't work, or at any point, if you run into difficulties, then stop and let your instructor know. They will help you set this up during the first couple days of class!
 
### [⇐ Previous](3_git.md) | [Back to README ⇒](../../../../)
