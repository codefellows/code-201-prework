# Setup for Ubuntu

----------------

This guide will help you setup a software development environment on <a href="http://releases.ubuntu.com" target="_blank">Ubuntu</a>. By the end, your computer will be configured with the same state-of-the-art tools used by professional software developers.

This guide is mostly compatible with older versions of Ubuntu. So follow along as best you can while Googling any problems you come across.


### The Terminal

Included in Ubuntu is the **Terminal** -- an app that runs a Unix shell.

A **Unix shell** (often referred to as a "terminal") is a command line user interface between you and your computer's operating system. 


### Explore the Terminal

Let's get our hands dirty and have some fun. First, use the Dash to launch the Terminal app.

![](https://i.imgur.com/qH7fROg.png)

Once launched, you'll see something like this.

![](https://i.imgur.com/DObOFyg.png)

### Change the Terminal Profile

The default profile for the Terminal looks pretty, but uses small text and has low color contrast. Let's change that.

First, run the following command to update your operating system's software. To run a command, type it into the Terminal and hit "enter". If you want to copy and paste commands into your prompt, you'll need to right-click on main Terminal window, and select "Paste". Or, you can press Control-Shift-V.

```
sudo apt-get update
```

**TIP:** This will require your account password which **will not** appear on the screen as you type, but tracks your key-strokes.

Then run this command to install a handy command line program called `curl`, which we'll use in a second.

```
sudo apt-get install -y curl
```

Then download and install the new Terminal Profile.

```
curl -fsSL http://git.io/Ak1LNQ | sh
```


Then navigate to the Terminal's `Edit > Profiles` menu item.

![](https://i.imgur.com/urVA5BE.png)

In the `Profiles` window, select `Tomorrow` as the profile used when launching a new terminal.

![](https://i.imgur.com/8oemVp3.png)

Finally, quit and relaunch the Terminal. Now, every new Terminal window will look like this.

![](https://imgur.com/JCIdYi7.png)


### [Next ⇒](2_apt.md)
