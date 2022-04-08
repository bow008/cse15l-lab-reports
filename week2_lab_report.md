# Week 2 Lab Report
This is a tutorial about how to log into a course-specific account on `ieng6`. There are 6 steps.
<!--- <span style="color:green">ieng6</span> --->
---
## Step 1: Installing VScode
If you haven't installed Visual Studio Code yet, the first step is to go to the [Visual Studio Website](https://code.visualstudio.com/) and follow the instructions to download and install it on your computer.

When it is installed, you should be able to open a window that looks like this (it might have different colors, or a different menu bar, depending on your system and settings):

![image](vscode.png)

---
## Step2: Remotely Connecting
> If you are on Mac, ignore this. If you are on Windows, you need to first install a program called [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).

**substep 1**: Look up your course-specific account for CSE15L [*here*](https://sdacs.ucsd.edu/~icc/index.php).

**substep 2**: Open your terminal. You can open your terminal in VS Code (Ctrl + `).

**substep 3**: Enter the following commend in terminal, <mark >but with the `zz` replaced by the letters in your course-specific account:</mark>

`$ ssh cs15lsp22zz@ieng6.ucsd.edu`

If this is your first time connecting to the server, you'll get a message like this:

` ⤇ ssh cs15lsp22zz@ieng6.ucsd.edu`

`The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.`

`RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.`

`Are you sure you want to continue connecting
(yes/no/[fingerprint])?`

You should type `yes` and press "Enter".

**substep 4**: Now, you will be prompted to enter your password. Don't freak out if your password don't show up on the screen when you type it; just type your password and press "Enter".

> After doing all of the above 4 substeps, your terminal will probably be connected to a computer in the CSE basement, and you'll receive a message like this:
![image](server.png)
And that's it!
---
## Step 3: Trying Some Commands
Now you can practice what you've learned in lectures! Try some commands, both on the remote computer and on your own computer. 

> To go back to your own computer, you can log out by typing `exit` and then press "Enter":
![image](exit.png)

Here are some specific useful commands to try:

* `cd ~`
* `cd`
* `ls -lat`
* `ls -a`
* `ls <directory>` where `<directory>` is
`/home/linux/ieng6/cs15lsp22/cs15lsp22abc`, where the `abc` is one of the other group members’ username
* `cp /home/linux/ieng6/cs15lsp22/public/hello.txt ~/`
* `cat /home/linux/ieng6/cs15lsp22/public/hello.txt`

---

## Step 4: Moving Files with `scp`
Now if we want to copy a file from your computer to a remote computer, we can run the command `scp` from the *client* (that means from your computer, not logged into `ieng6`).


