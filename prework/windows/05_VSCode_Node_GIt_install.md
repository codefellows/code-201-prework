# Installing VSCode, Node.js, and Git

After finishing this doc you will have VSCode, Node.js, and Git installed on your machine.

## VSCode

1. Vist [VSCode](https://code.visualstudio.com/?wt.mc_id=adw-brand&gclid=Cj0KCQjw5-TXBRCHARIsANLixNw00R2vbdqnzLml-GvzCgbyqmgcAb9kyRQsC5LAPVS6tuBDZ9ws9pgaAsiLEALw_wcB) to download VSCode.
1. Launch the installer and follow the onscreen prompts.
1. **When you reach the section for `Additional tasks`, make sure every box is checked.**
1. Click install and continue to follow and onscreen prompts.

Once you are done, you can open up a terminal (the Ubuntu App) and type `code` to open VSCode. This may or may not require a restart first. 

## Node.js - Version 10.x

1. Open the Ubuntu app and type `cd ~` to bring you into the Ubuntu FS.
1. Type `sudo apt-get update`. This will tell Ubuntu's apt tool to update.
1. After it is done updating run the command:

```
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
```

then run:

```
sudo apt-get install -y nodejs
```

We will also install Node on Windows:

1. Visit <https://nodejs.org/en/download/> and download and run the Windows installer.

## Eslint

1. Search 'windows powershell' in the start menu and open it.
2. Run `npm i -g eslint` . When finished close windows powershell.

## Git

Git is already installed on Ubuntu as it comes built in. VSCode however also uses Git for it's source-control tool to work. But since VSCode is a Windows application, it doesn't know how to use Ubuntu's version of Git. 

1. Visit [git-scm.com](https://git-scm.com/) to download and install Git.
2. Follow the onscreen instructions.

    - Choose the default values for each prompt...
    - **EXCEPT** when it asks you to `Choose the default editor used by Git`... 
        - click the drop down and choose the VSCode option
        - Do NOT choose the "VSCode Insiders" option. 
    - This will allow you to handle merge conflicts in your editor instead of in your command line which is another reason to have Git on Windows as well.

3. Continue choosing the default options to finish the installation.

### Set the Git Config

The final step here is to add your email and name to the Git config. This will allow you to commit and push things to GitHub. Make sure to include the space after `.email` and `.name`, and always remember to close your quotes ' ' and " ".

1. Close and re-open a new Ubuntu terminal
1. Type `git config --global user.email 'your email here in single quotes'`.
1. Type `git config --global user.name 'Your Name In Single Quotes'`.
1. Type `git config --global core.editor 'code --wait'`.

### [⇐ Previous](./04_updating_terminal.md) | [Next ⇒](./06_final_steps.md)
