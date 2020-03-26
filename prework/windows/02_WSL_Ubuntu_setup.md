# Setting up WSL and the Ubuntu app

**Before you begin check to make sure that you have the [most recent version of Windows 10](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-update).**

**You are not expected to understand what is taking place as you complete the steps in this guide. It is important that you do not skip ahead.  Please follow the instructions line by line.**

## Overview  
 
Windows does not run in a POSIX environment. Much of the software you use as a developer is designed to run in POSIX environments, and many of the web's servers are also running in some POSIX environment. This causes problems because Windows uses different console commands and not all of those commands translate over to POSIX very well.

Windows has released a feature available to all PCs running on Windows 10 called Windows Subsystem for Linux, otherwise known as WSL. WSL gives you the ability to add a Linux distro like Ubuntu and mount it directly to the Windows File System.

**Ubuntu can _read and write_ both** Ubuntu and Windows files, **Windows can only _read and write_ Windows files**, and **_read_ Ubuntu Files**, but it **_cannot_ write Ubuntu files**. Knowing which files belong to which FS is important because of this.

Before we dive into how to use the Ubuntu App and WSL, lets talk about one of the most important things, which is **knowing your File Systems**

There are 2 files systems here:

1. The Windows FS
2. The Ubuntu FS.


## Install Instructions:

### Please read through these steps before getting started

**Follow the instructions line for line, pay attention to detail!!**

#### 1. Enable WSL Feature in Windows.

1. Right click on the start menu and click on Settings.
2. In the Search box, type `Turn Windows Features On Or Off` and click on the item that populates in the list.
3. A window will pop up with a list of folders with checkboxes next to them. Scroll down and check the box for `Windows Subsystem for Linux`.

This will install the needed files. Follow any directions that pop up and restart when asked. This page might not open after restart, so be sure to make note of the url or bookmark it.

#### 2. Install the Ubuntu app from the Windows Store.

1. Click here to go to Microsoft store and install the [Ubuntu App](https://www.microsoft.com/en-us/store/p/ubuntu/9nblggh4msv6?activetab=pivot%3aoverviewtab)
1. Follow the on-screen prompts to install the app. 
1. When the app is ready, it will say Launch. Click Launch. This will start the Ubuntu installation. This installation only happens the first time the app is launched, as it's the actual Ubuntu OS installing and mounting to your Windows FS. Anytime you uninstall the app and reinstall it you will have to do this process again. Make sure to back up important data if you ever uninstall this app, as it is not preserved. 

#### 3. Finish Installing the Ubuntu App.

1. It will ask you to enter a username. This will be the root / admin user for the Ubuntu FS. 
1. It will then ask you to enter and confirm a password. It's recommended it's not too long as you may have to type it a lot. Also note that it will protect your password by not displaying it to the screen when you type, but it is registering your key strokes.
1. Finally, the prompt will change and you will be on a command line. Type `pwd` to see where you currently are in the FS, you should be at `/home/<your username>`. **This is the root level of your Ubuntu user.**

#### 4. Updating Default Software.

1. Type `sudo apt-get update`.
1. Once that is complete, type `sudo apt-get upgrade`. Press `y` when prompted. 
1. Once that is done, type `sudo apt autoremove`. This will remove any packages that are no longer needed.

At this point you are now totally setup with WSL and the Ubuntu app.

- Open the Ubuntu app and type `pwd`. Assumuing you haven't changed anything yet, you'll notice that it says something like `/home/<your username>`.

This `/home/` means that you are in the Ubuntu FS. 

### [Next ⇒](./04_updating_terminal.md)
