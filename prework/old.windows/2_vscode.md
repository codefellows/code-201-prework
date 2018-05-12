### Install VSCode Text Editor

Now it's time to install VSCode Text Editor, a sophisticated text editor for code, markup, and prose.

To get started, download [VSCode](https://code.visualstudio.com/download) and run the installer. Again, go with the default installation options, unless you really know you want to change something.

[VSCode's documentation](https://code.visualstudio.com/docs) is excellent. Review it now to familiarize yourself with the basics.

Once installed, use the Start Menu to launch VSCode.

### Install Shell Commands

You'll find it useful to open files and directories into VSCode from the Terminal.

Launching from the Command Line# You can also run VS Code from the terminal by typing 'code' after adding it to the path: Launch VS Code. Open the Command Palette (Ctrl+Shift+P) and type 'shell command' to find the Shell Command: Install 'code' command in PATH command.

To verify VSCode is wired up correctly, run the `code` command from your command line.

If VSCode opens, you're good to go.

If VSCode does not open, try the above process again. If it still does not work, we will remedy it during lab on the first day of class. 

### Associate VSCode with Git

It's important to establish a default editor with Git, as it's the program that will be used to open up all of your files.

Type the following command in your terminal:
`git config --global core.editor "code --wait"`

If you have any problems, make note of them and we will address them in lab on the first day of class.


### [⇐ Previous](1_terminal.md) | [Next ⇒](3_git.md)
