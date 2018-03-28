# Windows 201 WSL setup

Before you begin check to make sure that you have the [Fall Creators Edition of Windows 10](https://support.microsoft.com/en-us/help/4028685/windows-10-get-the-fall-creators-update).

This will guide you through setting up the Windows Subsystem for Linux ( WSL).

--- 

Quick links:

1. [Update terminal profile](https://gist.github.com/michaeltreat/56bc49f1dd61427cb3d9424c774a2486)
2. Git (currently missing)
3. VSCode ( currently missing)
4. [Node Install](https://gist.github.com/michaeltreat/2219f2e4126b7c4417017a4504220dc7)
5. [PostgreSQL 10 Install](https://gist.github.com/michaeltreat/40a2f444d8ff6c89af958733448da093)
6. [MongoDB Install](https://gist.github.com/michaeltreat/a6d73f6a0fff6dadf3ea6a472191eb61)

---

### Preface

WSL stands for Windows Subsystem for Linux, and what it does is allows us to use our Windows file system in a POSIX environment. This allows us to use a bunch of software that may be limited to Linux or Unix-like systems. Since many of the servers on the web are also running in Unix-like environments, this tool is a huge boost to Windows Web Development. 

After following these instructions, you will have a Ubuntu Subsystem on your machine. What that means is that Ubuntu will be attached (mounted) to your C: drive, and it will act just like it's own Operating System. The great thing is that it can access your Windows Files so that you can run any software in a POSIX environment for you.

A couple things to note:

1. There will be 2 file systems here: 
  - The Ubuntu File System
  - The Windows File System
  - And Both have access to each other.
2. Both File systems work together with each other.
  - The Ubuntu file system is used to install and run programs and software.
  - While the Windows File system is used to hold all of the files and repos that you are working on. 
3. This is because while you can use the Ubuntu File system to edit Files in Windows, You CANNOT use Windows to edit file in the Ubuntu Subsystem.
  - This is important. Since you cannot edit Ubuntu files from Windows or Windows Apps, all of the work you do should be done on the Windows File systems. This way both Windows and Ubuntu can access them.
  - And likewise, any of your software setups should be done on Ubuntu. This is so you can run these programs in a POSIX environment. If you ever do have to edit files in Ubuntu then you need to use the nano editor that comes with Ubuntu, or install you own commandline editor for Ubuntu.
  - The exception to this is your main code editor. You should still install VSCode or whichever editor you use through Windows so you have a good editor for the files you'll be working on in Windows
5. At this point, there is very very little difference between using the Ubuntu app vs using the Windows PowerShell WSL. Both are running Ubuntu. WSL by default looks at which distro you have installed (Ubuntu, Fedora, Debian) and runs that. Since we only have Ubuntu, that's what it's running.
6. If you entered in through the PowerShell WSL then you will start in the Windows File System. If you entered through the Ubuntu app, then you will start in the Ubuntu File System. Regardless of where you start, you can navigate to either file system very easily. See tips below for more info on this.
6. You will spend the vast majority of your time in the PowerShell WSL on the Windows File System as this is where you will be doing your work. You will only need to spend time in the Ubuntu File System when you need to install new software or want to update your terminal window. The rest of the time will be spent in WSL on the Windows File System.

### WorkFlow:

Once everything is installed, it is recommended that you use the Windows PowerShell and type `wsl` to enter the Windows File System while using the Windows Subsystem for Linux.

---

## Install Instructions:

Please read through these step once before starting!

---
### 1. Enable WSL Feature in Windows.

1. Right click on the start menu and click on settings.
2. In the Search box, type `Turn Windows Features On Or Off` and click on the item that populates in the list.
3. You will see a list of folders with checkboxes next to them. Scroll down and check the box for `Windows Subsystem for Linux`.

This will install the needed files. Follow any directions that pop up and restart when asked.

### 2. Install the Ubuntu app from the Windows Store.

1. Click here to go to Microsoft store and install the [Ubuntu App](https://www.microsoft.com/en-us/store/p/ubuntu/9nblggh4msv6?activetab=pivot%3aoverviewtab)
2. Follow the on-screen prompts and just select the default values.
3. Restart when installation is complete.

### 3. Finish Installing the Ubuntu App.

1. Open the Ubuntu app. ( If you can't find it, then right click on the start menu and click search, then type in Ubuntu.)
2. The app will begin to install in a terminal window. It will eventually propmt you for a user name, a password, then to confirm that password. ( You may be typeing this password quite a bit, so maybe make it short :D ) TAKE NOTE! This will be your user name and password whenever you need to do things in Ubuntu. 

### 4. Using WSL

At this point you are now able to use the Windows Subsystem for Linux through using the Ubuntu Distro. It is recommended though that you instead use WSL throguh the windows PowerShell instead of using the Ubuntu app itself. 

1. Right click on the start menu and select `Windows PowerShell`. 
2. When the screen has loaded, type `wsl`. This will enter you into a Ubuntu Shell, which will give you access to a POSIX environment, and POSIX commands. 

Note that you are actually starting in the Windows File System here, and when you launch the Ubuntu app you are starting in the Ubuntu app's file system. Since we cannot edit Ubuntu files with VSCode, we are going to use WSL through the PowerShell instead, and we are going to be creating our files on the Windows File System, not the Ubuntu file system.

And you're done! Using the Windows Subsystem for Linux will allow you to use and Ubuntu terminal for you work.


### Quick tips

1. Ubuntu is actually a Sub file system that is attached ( mounted ) onto the C: drive of Windows. It's typically found here: 
`C:\Users\<user>\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState\rootfs`.
2. You cannot edit Ubuntu's files through Windows or through a windows app. If you want to edit an Ubuntu file you should use the Ubuntu CLI editor tool nano IE `sudo nano test.js`.
3. While you cannot edit Ubuntu files, Ubuntu can edit Windows files all it wants! When you are in the Ubuntu app you can access the Windows file system by going to the root of the Ubuntu file system and then moving to `/mnt/c/`.
4. Here's a link to some [FAQ](https://docs.microsoft.com/en-us/windows/wsl/faq)
5. You will still have to install some programs in the Ubuntu File System through the command line ( like Node for 201, and Postgres, Heroku cli for 301, etc.) When you reach these points you should follow the Ubuntu installation instructions for that specific program if a Windows specific install is not provided.
6. Update your terminal window to give you a better interface in [this doc](https://gist.github.com/michaeltreat/56bc49f1dd61427cb3d9424c774a2486).
