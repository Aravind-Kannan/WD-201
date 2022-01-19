# Web Development 201 - Django Course

## Level 1: Getting started with Git

- Installing Git
- Terminal crash [course](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line)

  - **Where did the terminal come from?** <br>
    The terminal originates from around the 1950s-60s and its original form really doesn’t resemble what we use today. Since then, the terminal has remained a constant feature of all operating systems. It provides direct access to the computer’s underlying file system and low-level features, and is therefore incredibly useful for performing complex tasks rapidly, if you know what you are doing.It is also useful for automation — for example to write a command to update the titles of hundreds of files instantly, say from “ch01-xxxx.png” to “ch02-xxxx.png”. If you updated the file names using your finder or explorer GUI app, it would take you a long time.
  - **What does the terminal look like?**
    - In Windows: "cmd" & "powershell"
    - In MacOS: "terminal"
  - **How do you access the terminal?** <br>
    - In Linux: Linux/Unix systems have a terminal available by default, listed among your `Applications`.
    - In MacOS: macOS has a system called **Darwin** that sits underneath the graphical user interface. Darwin is the Unix-like system, which provides the terminal, and access to the low-level tools. The terminal is available on macOS at `Applications/Utilities/Terminal`.
    - In Windows: `CMD` or better known as "command prompt" doesn't have parity with Unix commands, and is equivalent of a `DOS prompt`. Better programs exist for providing a terminal experience on Windows, such as `Powershell`, and `Gitbash`. However, the best option for Windows in the modern day is the `Windows Subsystem for Linux (WSL)` — a compatibility layer for running Linux operating systems directly from inside Windows 10, allowing you to run a “true terminal” directly on Windows, without needing a virtual machine.
    - Side note: what's the difference between a command line and a terminal? [Refer website]
  - **Basic built-in terminal commands:**
    - Navigate your computer’s file system along with base level tasks such as create, copy, rename and delete:
      - Move around your directory structure: `cd`
      - Create directories: `mkdir`
      - Create files (and modify their metadata): `touch`
      - Copy files: `cp`
      - Move files: `mv`
      - Delete files or directories: `rm`
    - Download files found at specific URLs: `curl`
    - Search for fragments of text inside larger bodies of text: `grep`
    - View a file's contents page by page: less, cat
      Manipulate and transform streams of text (for example changing all the instances of `<div>`s in an HTML file to `<article>`): `awk`, `tr`, `sed`
  - `Tab` key comes in handy as an auto-complete feature
  - Relative vs Absolute Paths
  - `dir` in Windows equivalent of `ls` in Linux
  - To find out exactly what options each command has available, you can look at its `man page`. This is done by typing the `man` command, followed by the name of the command you want to look up, for example `man ls`.
  - To run a command with multiple options at the same time, you can usually put them all in a single string after the dash character, for example `ls -lah`, or `ls -ltrh`
  - `rmdir -r` would delete the directory and its contents _recursively_. Just be sure before deleting.
  - `mv` for moving and renaming.
  - Many terminal commands allow you to use asterisks as "wild card" characters, meaning "any sequence of characters". This allows you to run an operation against a potentially large number of files at once, all of which match the specified pattern. `rm mdn-*.bak` would delete all files that start with `mdn-` and end with `.bak`.
    > 🤑 **Why does Windows use backslash instead of forward slash**: Digital Equipment Corporation made a design choice to use forward slash for [cmd line switches](https://support.microsoft.com/en-us/office/command-line-switches-for-microsoft-office-products-079164cd-4ef5-4178-b235-441737deb3a6) which was carried forward to CPM, then to MS DOS 1.0, but in MS DOS 2.0 Directories came into existence, so people thought it would be nice idea to use back slash as directory separator. (and everything was okay, but since devs wanted forward slash as directory separator, the switches went from forward slash to hyphen)
  - ❤️ [tl;dr](https://tldr.sh/) is simplified version of `man` pages
  - **Connecting commands together with pipes**: Using pipes take the output of the first command's execution and pass it as input onto the next command after the pipe. A general philosophy of (unix) command line tools is that they print text to the terminal (also referred to "printing to standard output" or `STDOUT`). A good deal of commands can also read content from streamed input (known as "standard input" or `STDIN`). The `pipe operator` can `connect` these inputs and outputs together, allowing us to build up increasingly more complex operations to suit our needs — the output from one command can become the input to the next command.
  - **Adding powerups**: The vast ecosystem of installable tools for front end web development currently exists mostly inside `npm`, a privately owned, package hosting service that works closely together with Node.js. This is slowly expanding — you can expect to see more package providers as time goes on. Installing `Node.js` also installs the `npm` command line tool (and a supplementary npm-centric tool called `npx`), which offers a gateway to installing additional command line tools. Node.js and npm work the same across all systems: macOS, Windows, and Linux.
  - **Installing CLI Tools**
    - [Global vs Local](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line#where_to_install_our_cli_tools)
    - [Installing Prettier](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line#installing_prettier)
    - [Playing with Prettier](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line#playing_with_prettier)

- Intro to visual studio code
- Introduction to git:
  - **Version control systems** are vital to almost every development workflow.
  - Git is one of the most widely used version control system in the world, it is developed by the same guy who built the Linux operating system kernel **(Linus Torvarlds)** and it is an essential prerequisite for almost all software development related jobs out there.
- Prerequisites for Github: Creating an account on the github platform
- Collaborative Development with Github: Working on the local directory, staging area and remote repository
- More comprehensive tutorial at [Git-it](http://jlord.us/git-it/index.html)

  - Git is open source software (free for anyone to use) written by Linus Torvalds who also wrote the Linux operating system. It is a program for keeping track of changes over time, known in programming as **version control**.
  - Dollar signs $ are often used in programming documentation to signify that the line is command line code (see the code snippets above). You don't actually type the $ in though, only type what comes after. For instance, to run the verify command above, you're actually going to type git-it verify into terminal.
  - Summary of the commonly used commands:

  ```bash
  # Chapter 1 - Get git : Installing git on your local machine

  # Chapter 2 - Repository

  # Make a new folder (aka directory)
  $ mkdir <FOLDERNAME>
  # Navigate into an existing folder (aka change directory)
  $ cd <FOLDERNAME>
  # List the items in a folder
  $ ls
  # Turn Git on for a folder
  $ git init

  # Chapter 3 - Commit to it

  # Check status of changes to a repository
  $ git status
  # View changes to files
  $ git diff
  # Add a file's changes to be committed [into staging area]
  $ git add <FILENAME>
  # To add all files changes [into staging area]
  $ git add .
  # To commit (aka save) the changes you've added with a short message describing the changes
  $ git commit -m "<your commit message>"

  # Chapter 4 - GitHubbin

  # A common error is not having your GitHub username match the case of the one you set with git config. For instance, 'JLord' isn't the same as 'jlord'. To change your username set with Git, just do the same command you did earlier, but with the correct capitalization:
  $ git config --global user.username <USerNamE>

  # Chapter 5 - Remote Control

  #Add remote connections
  $ git remote add <REMOTENAME> <URL>
  # Set a URL to a remote
  $ git remote set-url <REMOTENAME> <URL>
  # Pull in changes
  $ git pull <REMOTENAME> <BRANCHNAME>
  # View remote connections
  $ git remote -v
  # Push changes
  $ git push <REMOTENAME> <BRANCH>

  # Chapter 6 - Forks and clones

  # After you FORK the ORIGINALREPO [upstream] into your account, you willl get a URLFROMGITHUB [origin], you can clone this local repository
  $ git clone <URLFROMGITHUB>
  $ git remote add upstream <ORIGINALREPO>

  # Chapter 7 - Branches aren't just for birds

  # You can create and switch to a branch in one line:
  $ git checkout -b <BRANCHNAME>
  # Create a new branch:
  $ git branch <BRANCHNAME>
  # Move onto a branch:
  $ git checkout <BRANCHNAME>
  # List the branches:
  $ git branch
  # Rename a branch you're currently on:
  $ git branch -m <NEWBRANCHNAME>
  # Verify what branch you're working on
  $ git status

  # Chapter 8 - It's A Small World : Adding Colloborators to the repository using GitHub settings

  # Chapter 9 - Pull Never Out Of Date

  # Check Git status
  $ git status
  # Pull in changes from a remote branch
  $ git pull <REMOTENAME> <REMOTEBRANCH>
  # See changes to the remote before you pull in
  $ git fetch --dry-run

  # Chapter 10 - Requesting You Pull Please : Creating pull requests using the GitHUb interface to the ORIGINALREPO

  # Chapter 11 - Merge Tada

  # Merge a branch into current branch
  $ git merge <BRANCHNAME>
  # Change the branch you're working on
  $ git checkout <BRANCHNAME>
  # Delete a local branch
  $ git branch -d <BRANCHNAME>
  # Delete a remote branch
  $ git push <REMOTENAME> --delete <BRANCHNAME>
  # Pull from a remote branch
  $ git pull <REMOTENAME> <BRANCHNAME>

  ```

  - Chapter 5 - More on [Remote control](http://jlord.us/git-it/challenges/remote_control.html)
  - Chapter 6 - More on [Forks and clones](http://jlord.us/git-it/challenges/forks_and_clones.html)
