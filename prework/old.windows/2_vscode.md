## Install VSCode Text Editor

Now it's time to install VSCode Text Editor, a sophisticated text editor for code, markup, and prose.

To get started, download [VSCode](https://code.visualstudio.com/download), and after it is installed, launch the application.

[VSCode's documentation](https://code.visualstudio.com/docs) is excellent. Review it now to familiarize yourself with the basics.

### Install shell commands

In Windows, installation of VSCode should automatically install a terminal shortcut to open the application by entering the command `code`, or to open all files in a directory, `code .`. Try this, and if it does not work on your laptop, we will remedy it during lab on the first day of class. 

### Associate VSCode with Git

It's important to establish a default editor with Git (version control software) so that when Git opens files, that happens in your chosen editor.

Type the following command in your terminal:
`git config --global core.editor "code --wait"`

This command will not return any message unless there is an error.

### Install Node

To install Node, go [here](https://nodejs.org/en/download/), and then download and run the Windows Installer. Make sure you do not deselect any of the Node components such as NPM during the installation.

If you run into issues trying to install Node from these steps, please contact your instructor.

It will take a few minutes for the download and installation process to complete.

#### Verify the Node installation

Now let's verify that it is installed. Enter the following into your terminal:

`node -e 'console.log("works")'`

You should get a response that says "works". If not, try reinstalling Node again. If you are still having issues, please contact your instructor.

### Install ESLint

Now that you have Node installed, you can install Node packages using its package manager, **NPM**. Open your terminal (Git Bash on Windows) and enter:

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

### [⇐ Previous](1_terminal.md) | [Next ⇒](3_git.md)
