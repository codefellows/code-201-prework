### Verify Git

If you've been following along with this guide, you've already installed Git, the version control system of choice among choosy developers.

To verify, run the following command. To run a command, type it into the command prompt in Git Bash and hit "enter". If you want to copy and paste commands into your prompt, you'll need to right-click on main Git Bash window, and select "Paste". Or, you can press the Shift and Insert keys.

```
git --version
```

And you'll see something like this.

![](https://i.imgur.com/fnUU61q.png)

### Git Config

You're on the home stretch now! :racehorse:

Like artists, programmers sign their work. Let's configure Git to sign your commits with your name and email address.

Sign up for an account at Github <a href="https://github.com" target="_blank">here</a>.

**WARNING:** Before running the following commands, replace `YOUR FULL NAME` and `YOUR EMAIL ADDRESS` with the name and email from <a href="https://github.com/settings/profile" target="_blank">your GitHub account</a>.

```
git config --global user.name 'YOUR FULL NAME'
git config --global user.email 'YOUR EMAIL ADDRESS'
```

The terminal does not send success messages, in order to double check that you have successfully assigned your username and email:

```
git config --list
```

Your terminal should output the following lines:

```
user.email='YOUR EMAIL ADDRESS'
user.name='YOUR FULL NAME'
```

### Congratulations!

You have now completed Step 3 of 9 in the Code 201 pre-work. Please follow the README link below to complete the remaining steps (4-9).

### [⇐ Previous](2_vscode.md) | [Back to README ⇒](../../../../)
