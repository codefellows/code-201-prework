Setup for Windows
-----------------

This guide will help you setup a software development environment on <a href="http://windows.microsoft.com/en-us/windows/products" target="_blank">Windows 7</a> and above. By the end, your computer will be configured with the same state-of-the-art tools used by professional software developers.

This guide is mostly compatible with older versions of Windows. So follow along as best you can while Googling any problems you come across.


### The Terminal

A **Unix shell** (often referred to as a "terminal") is a command line user interface between you and your computer's operating system. In a Unix shell, you can type in commands that tell the computer to do many things: navigate to files and folders, install and run programs, and change configurations. Programmers rely on their Unix shells to do lots of work, quickly and easily.

You're probably most familiar with the graphical user interface (the "GUI") of your computer's operating system. Those are the boxes, windows, and menu items that you click on with your mouse. While that's technically a shell too, most programmers think of the textual, command line interface when they hear to word _shell_.

Sadly, Windows **does not** include a Unix shell. Let's fix that.

CAVEAT: Until Windows adopts more Unix standards, please be aware that any Unix-based tools written for Windows will inevitably have some quirks.


### Install Git for Windows

<a href="http://msysgit.github.io/" target="_blank">Git for Windows</a> brings the full feature set of Git to Windows. (More on Git in a moment.) It also includes **Bash**, a popular Unix shell. Besides giving you the ability to talk to your computer by typing commands, it also lets you use Git in the command line, just like other Unix environments.

What's Git? It's a very popular **version control** system. Version control systems let programmers share and collaborate on code. With Git, multiple programmers can work on the same files, and Git keeps track of who made what changes, when. Git is usually used with a website, GitHub, that stores code (in "repositories") and lets programmers review and discuss changes before they are added. In short, Git makes everyone's lives easier.

To get started, download <a href="http://msysgit.github.io/" target="_blank">Git for Windows</a>. Once you click the "download" button, you'll see a list of download options.

Look closely at the first two filenames in the list. One says "32 bit", and the other says "64 bit". Those are the different versions for 32-bit and 64-bit Windows. Download the one for your system. If you don't know whether your version of Windows is 32- or 64-bit, <a href="http://windows.microsoft.com/en-us/windows/32-bit-and-64-bit-windows" target="_blank">find out</a>.

Once you get it downloaded, double-click the file to open the installer. It will guide you through several options; the defaults are just fine, so keep on clicking "Next" until it's done.

When it's done installing, use the Start Menu to launch Git Bash. **TIP:** search for and open "Git Bash", not "Git CMD" or "Git GUI". Then, pin it to your Start Menu so it's easy to find.

![](https://i.imgur.com/9CKUGs5.png)

After it's launched, you'll see something like this.

![](https://i.imgur.com/hyjvQkW.png)

Ignoring the welcome message and the git help, here's a quick break down of what you're seeing in the Terminal app.

| Component             | Description                            |
| --------------------- | -------------------------------------- |
| `Ryan Sobol`          | Name of your user account              |
| `PHOTON-PC`           | Name of your computer                  |
| `~` (home directory)  | Name of your working directory         |
| `$`                   | Prompt symbol                          |

Any characters you type will appear after the `$` prompt symbol. Go ahead and type `uname`. After pressing the Enter key, you'll see something like this.

![](https://imgur.com/muRRwcK.png)

Here's what happened:

1. The shell waited for you to type a command.
1. You then typed the word `uname` which appeared after the prompt.
1. You pressed the Enter key which triggered the shell to accept your input.
1. The shell searched for a program called `uname`.
1. Once found, the shell launched the `uname` program and handed it control over the Terminal.
1. While running, the `uname` program told the Terminal to display the word `MINGW32_NT-6.1`.
1. Once finished, the `uname` program exited and handed control of the Terminal back to the shell.
1. The shell told the Terminal to display another prompt.
1. Once displayed, the shell began waiting for your next command.

Simply stated, a Unix shell works in a read-evaluate-print loop or **REPL**.

### [Next ⇒](2_vscode.md)
