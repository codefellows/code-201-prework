Code 201: Computer Setup
-----------------------

### Overview of Computer Setup Steps *(time to complete per item)*

1. Laptop readiness *(time for this can vary widely depending upon the age and condition of your laptop)*
2. Setup Guide for Your OS *(multiple downloads are involved; 1-3 hours depending on your network speed)*

### Material Requirements

#### 1. Ensure your laptop is up to the task of coding specified in the [Code Fellows Material Requirements](https://www.codefellows.org/courses/code-201/foundations-of-software-development/#material-requirements)

> ##### *Chromebooks are not suitable for this course, most students use Macs* 

- 64-bit Operating System, like macOS or Windows 10
- Fully up to date, with the latest version of the operating system and all security updates installed
- At least 50GB of free space on the hard drive
- At least 8GB of RAM. 16GB RAM strongly preferred
- Free of viruses, and in general working order
- Can reliably connect to wireless networks

 
#### 2. Complete the setup guide for your computer's operating system

> ###### *CODE 101 DOES NOT COVER YOUR COMPUTER SETUP FOR 201. MAKE SURE TO FOLLOW THE ENTIRE SETUP GUIDE FOR YOUR OPERATING SYSTEM - Graduates of code 102 will have completed this computer setup step.* 

  - [Mac OS X](prework/mac/1_terminal.md)
  - [Windows 10](prework/windows/02_WSL_Ubuntu_setup.md)
  - [Ubuntu Linux(if you do not have Windows 10 or Mac OS)](prework/ubuntu/1_terminal.md)

#### By the time you’ve completed the guide, you should be able to run the following commands in your terminal:

- code --version
- git --version
- node --version
- npm --version
- eslint --version
- tree --version
- echo $PS1
- cat ~/.gitconfig

#### Each command should report a version number of what’s installed (should look *similar* to below example). Should you run across any errors that give you trouble please get a hold of contact below:

``` 
username@user $ code --version
1.40.2
f359dd69833dd8800b54d458f6d37ab7c78df520
x64
username@user $ git --version
git version 2.2.0
username@user $ node --version
v10.16.0
username@user $ npm --version
6.9.0
username@user $ eslint --version
v6.7.2
username@user $ tree --version
tree v1.8.0 (c) 1996 - 2018 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro
username@user $ echo $PS1
\[\e[36m\]\A\[\e[m\] \[\e[32m\]\w\[\e[m\] \[\e[37;40m\]`parse_git_branch`\[\e[m\]
username@user $ cat ~/.gitconfig
[core]
	editor = code --wait
[user]
	name = yourgithubusername
	email = youremail
username@user $ code
//should open VSCode
```
---

#### Need help or have questions about computer setup?

Please contact our Admissions Support Instructor.

If Code 102 self-paced isn't right for you, we understand. Ask about Code 102 (day or night classes) in a classroom setting with guidance. You’ll receive 30 hours of instruction as you blast through the prework for Code 201, while getting a tour of the tools and techniques of modern developers..


