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

## Level 2: Introduction to Python

- Setting up developer environment: `VSCode` and `Python`
- Running python code:
  - Running python shell (Python Interpreter): Based out of Read–eval–print loop
  - Executing python files
- Autoformatting used: Black, [instructed](https://marcobelo.medium.com/setting-up-python-black-on-visual-studio-code-5318eba4cd00) to install

  ### Getting started with Python

  - **What is Python?**: Python is an _interpreted, object-oriented, high-level_ programming language. Python is easy to get started with and is powerful enough to run large web applications.
  - **What is a Program?**: A program is a collection of statements that performs a specific task. or in simple words, it is an abstraction that takes some input and processes it to produce some output.
  - Variable names should:
    - be in **snake_case**
    - not start with a **number**
    - not be a **reserved keyword**
  - **Variables and Data types**:
    ```python
    number = 5 # int
    ratio = 1.5 # float
    salutation = "Hello" # string
    is_even = True # boolean
    ```
  - **Converting Data types**:
    - The process of converting one data type to another is called type conversion.
    - `type(<variable>)`: Returns the type of the `variable`
    - **Implicit type conversions** are done automatically by Python
    - **Explicit type conversions** are done manually in code
      - `int()`, `float()`, `str()`, `bool()` converts a given data type into the respective function's datatype
      - **Note**:
        - that converting a float to an int will truncate the decimal part of the number (Flooring the number)
        - trying to convert a non-numeric string to an int will result in an exception
  - **Strings in python**:
    ```python
    some_string = "hello world, This is A test"
    print(some_string.capitalize())  # Capitalizes the first character
    print(some_string.count("a")) # Counts the number of times the character "a" occurs in the string
    print(some_string.endswith("test")) # Returns True if the string ends with the substring "test"
    print(some_string.find("gem")) # Returns the index of the first occurrence of the substring "gem" and -1 if it does not exist.
    print(some_string.index("test")) # Returns the index of the first occurrence of the substring "test" and raises an exception if it does not exist.
    print(some_string.upper()) # Returns a copy of the string in uppercase
    print(some_string.title()) # Returns a copy of the string in title case
    print(some_string.swapcase()) # Returns a copy of the string in swapcase
    ```
  - **Note**: A neat little hack in Python to see all the functions available is to type `dir()` and see what functions are available.
  - **F strings**:
    - `F strings` are a relatively new addition to Python (since `3.6`), they are a way to format strings
      ```python
      some_variable = "john"
      print(f"hello {some_variable}") # prints hello john
      ```
  - **Blocks in python**: Python programs get structured through indentation, i.e. code blocks are defined by their indentation. it's a language requirement, not a matter of style.
  - **Functions in python [DRY principle - Don't repeat yourself]**:

    - Functions in Python are a group of statements (code block) that may or may not take inputs and may or may not return values.
    - At times, functions don't return any value, then they assume return type of `None`
    - To create functions without any statements in them use the `pass` statement

    ```python
    def greet(name, greeting = "Good Morning"): # this defines a function called greet with two parameters called name and greeting
      return greeting + " " + name

    print(greet("John")) # prints "Good Morning John"
    print(greet("Jane", "Good Afternoon")) # prints "Good Afternoon Jane"
    print(greet(name="John")) # we can also pass parameters to the function by name, that way we can change the order of the parameters
    ```

  - **Conditionals in python**:
    - A very simple if statement, has only one condition, if the condition evaluates as `True` or `1`, then the body of the if statement is executed, if not the body of the else is executed.
    ```python
    (2 > 1) and print("2 is greater than 1") # prints 2 is greater than 1
    (1 > 2) and print("1 is greater than 2") # prints nothing
    ```
  - **Lists**:

    - A list is a collection of items. These items can be of any data type. In Python, lists are very flexible as they allow to add/remove items if needed. Lists are mutable as in you can change the value of an item in a list.
    - Lists are indexed starting from `0`
    - Lists can be sliced (create a new sublist from the list) like this `list_variable[start:end]`, note that the `start` is included and the `end` is excluded
    - Lists can also be `negatively` indexed
    - 💡: To **interpret** _negative indices_ as positive, just convert to positive by _adding given -ve index to length of list_

    ```python
    list_with_numbers = [1, 2, 3, 4, 5]
    print(list_with_numbers[0]) # prints 1
    print(list_with_numbers[-1]) # prints 5
    print(list_with_numbers[-3:]) # prints [3, 4, 5] (the last three items with the start included)

    list_with_numbers.append(6) # adds 6 to the end of the list
    list_with_numbers.insert(2, 7) # inserts 7 at index 2
    list_with_numbers.remove(3) # removes the first 3 from the list ** Based on the value not the index
    list_with_numbers.pop() # removes the last item from the list
    list_with_numbers.pop(0) # removes the first item from the list
    list_with_numbers.reverse() # reverses the order of the list, note that this function does not return anything
    list_with_numbers.sort() # sorts the list , note that this function does not return anything
    list_with_numbers.sort(reverse=True) # sorts the list in reverse order

    some_string = "This is a test"
    list_of_words = some_string.split(" ") # The argument to the split function is used to split the words by.
    print(list_of_words) # prints ['This', 'is', 'a', 'test']

    list_of_words = ["This", "is", "a", "test"]
    joined_string = "-".join(list_of_words) # The argument to the join function is the list of words to be joined, "-" is the string that will be used to concatenate the list items.
    print(joined_string) # prints "This-is-a-test"
    ```

  - **Fun with lists**:

    - Given a list, we can define a function and have Python call the function with every item in the list. This is performed using the `map function`. Syntax: `map(<function>, <list>)`, returns a map, we must explicitly convert to list to use
    - Python comes with an immutable version of lists called `tuple`. Tuples do not support changes once initialized.

  - **Dictionaries**:

    - A dictionary in Python is simply a collection of key-value pairs.

    ```python
    contact_details = {
        "John": "1234567890",
        "Jane": "0987654321",
    }
    print(contact_details.keys()) # prints ["John", "Jane"]
    print(contact_details.values()) # prints ["1234567890", "0987654321"]
    print(contact_details.get("Jane")) # prints 0987654321
    print(contact_details.get("Mary", "Not found")) # prints Not found
    ```

  - **Iterations in Python**: Iterative statements are used to execute a block of code multiple times, usually, until a given condition has been reached.

    - `while` loop: In case you do end up in an infinite loop use `control + c` key combination to stop the program execution. We can also `break` to come out of a loop at any point. Similarly, we can also cause the loop to skip over some code by using the `continue` statement.

      ```python
      i= 10
      while True:
          i = i - 1  # decrement i by 1
          if i == 5:
              continue
          if i == 0:
              break
          print(i)
      ```

    - `for` loop: The `for` loop is used to iterate over a sequence (lists, dictionaries, string, or anything iterable). `range(start, stop, step)` can be used to build a list of numbers to be iterated over.

    > **Advanced Reading** : Python has a concept of iterators and generators. `Iterators` are objects that are used to iterate over a sequence. `Generators` are functions that return iterators. They are a bit hard to understand at first but once you get them you will understand them very well. You can find a full list of iterators and generators in the [Python documentation](https://docs.python.org/3/glossary.html#term-iterator).

    - **Exception Handling**:

      - Errors are called Exceptions in the Python world
      - The `try` block is the block that we want to execute, the `except` block is the code that we want to execute if an error occurs.
      - Note that the _statements after the error_ in the try block are _skipped_. Once an error occurs the rest of the try block is skipped and the except block is executed immediately.
      - We can also add generic exception handling by using the `except` keyword without specifying the exception type. This will handle all the exceptions that are not handled by the other `except` blocks. We can also add a `finally` block to the `except` block to execute code after the `try` block has been executed. The `finally` block is executed whether an _error occurs or not_
      - Exceptions in Python can also be raised by the programmer, this is done using the `raise` statement. This is useful when we want to force the execution to move to the except block.

      ```python
      try:
          numerator = 10
          denominator = 0 # Change this to see different execution flows
          if denominator > 100:
              raise ValueError("Denominator cannot be greater than 100")
          print("Answer is" , numerator/denominator)
      except ZeroDivisionError:
          print("You cannot divide by zero")
      except ValueError:
          print("Value Error! Denominator Must be < 100") # Catches the Value Error
      except:
          print("Something Happened")
      finally:
          print("All operations have been completed")
      ```

    - **Recursive Functions**: A function that calls itself and terminated by a `base case`.

    ```python
    def countdown(number):
        if number < 0:
            return
        print(number)
        countdown(number - 1)
    countdown(10)
    ```
