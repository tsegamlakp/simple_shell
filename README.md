<h1 align="center" >
<br>
    <img src="https://www.alxafrica.com/wp-content/uploads/2022/01/header-logo.png" height="50%" width="40%">
</h1>

<h2 align="center">



  
# Project 0x16. C - SIMPLE SHELL 📚

### Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

### General

* Who designed and implemented the original Unix operating system
* Who wrote the first version of the UNIX shell
* Who invented the B programming language (the direct predecessor to the C programming language)
* Who is Ken Thompson
* How does a shell work
* What is a pid and a ppid
* How to manipulate the environment of the current process
* What is the difference between a function and a system call
* How to create processes
* What are the three prototypes of main
* How does the shell use the PATH to find the programs
* How to execute another program with the execve system call
* How to suspend the execution of a process until one of its children terminates
* What is EOF / “end-of-file”?

****
## Table of contents
 - **What is the shell?**
 - **About this project**
 - **Essential Functionalities of the Simple Shell**
 - **File description**
 - **List of allowed functions and system calls for this project**
 - **USAGE**
 - **Example of Usage**
 - **Bugs**
 - **TEAM**
 ****

## What is the shell?
The shell is a program that takes commands from the keyboard via the terminal, and gives them to the operating system to perform.\



### 📋 Requirements
***
* Allowed editors: vi, vim, emacs
* All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
* All your files should end with a new line
* A README.md file, at the root of the folder of the project is mandatory
* Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
* Your shell should not have any memory leaks
* No more than 5 functions per file
* All your header files should be include guarded
* Use system calls only when you need to (why?)

### GitHub
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

## Essential Functionalities of the Simple Shell:
> Displays a prompt "#cisfun$ " and waits for user input.\
> Runs all commands of type "executable program" (ls and /bin/ls).\
> Runs the following build_in commands: **exit**, **env**, **setenv** and **unsetenv**.\
> Handles commands with arguments.\
> Handles the PATH global variable.\
> Handles The EOF (End Of File) condition.\
> Handles the Ctrl + C signal -> It doesn't exit the shell

## Files description
 - **AUTHORS** -> List of contributors to this repository
 - **man_1_simple_shell** -> Manual page for the simple_shell
 - **shell.h** -> Header file
 - **shell.c** -> main function
	- **sig_handler** -> handles the Ctrl + C signal
	- **_EOF** -> handles the End Of File condition
 - **string.c**
	- **_putchar** -> prints a character
	- **_puts** -> prints a string
	- **_strlen** -> gives the length of a string
	- **_strdup** -> copies a string in a newly allocated memory
	- **concat_all** -> concatenates 3 strings in a newly allocated memory
 - **line_exec.c**
	- **splitstring** -> splits a string into an array of words
	- **execute** -> executes a command using execve
	- **realloc** -> reallocates a memory block
	- **freearv** -> frees a 2 dimensional array
 - **linkpath.c**
	- **_getenv** -> returns the value of a global variable
	- **add_node_end** -> adds a node in a singly linked list
	- **linkpath** -> creates a singly linked list for PATH directories
	- **_which** -> finds the pathname of a command
	- **free_list** -> frees the linked list of PATH value
 - **checkbuild.c**
	- **checkbuild** -> checks if a command is a build-in command
 - **buildin.c**
	- **exitt** -> handles the exit buildin command
	- **_atoi** -> converts a string into an integer
	- **env** -> prints the current environment
	- **_setenv** -> Initialize a new global variable, or modify an existing one
	- **_unsetenv** -> remove a global variable
***
## USAGE
You can try our shell by following these steps:
> **Step 1:** Clone our repository using this command, (you need to have git installed on your machine first)
````
git clone https://github.com/MatriMariem/simple_shell
````
> **Step 2:** Change directory to simple_shell:
````
cd simple_shell
````
> **Step 3:** Compile the C files in this way:
````
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
````
> **Step 4:** Run the shell
````
./hsh
````
**Exiting the shell**
When you want to exit the shell, you can use one of the following methods:
> **1: Type the command "exit"**
````
exit
````
> **2: Press on Ctrl + D**


### List of comands you can use

| Commands | Description |
|--|--|
| `ls` | ls (from list), allows you to list the contents of a directory or file. |
| `pwd` | Pwd (from print working directory) is a convenient command that prints our path or location when executed, so we avoid getting lost if we are working with multiple directories and folders. |
| `touch` | touch creates an empty file, if the file exists it updates the modification time. |
| `rm` | rm (from remove) is the command needed to delete a file or directory. |
| `mkdir` | mkdir (from make directory) creates a new directory taking into account the current location. |
| `cp` | cp (from copy) copies a source file or directory to a target fileor directory. |
| `rmdir` | rmdir (from ReMove DIRectory) This command is used to delete empty directories or subdirectories. |
| `cd` | cd (from change directory) you will need this command to access a path other than the one you are in. basically it is for navigating from directory to directory. |
| `exit` | exits the current shell. 0 status value indicates successful execution, another value represents unsuccessful execution. |
| `cat` | cat (from concatenate), is a wonderful utility that allows us to visualize the content of a text file in the standard output, without the need of an editor. |

   <p align="center">
Mohammed Bheser -
<a href="https://github.com/123mame">
        <img src="https://avatars.githubusercontent.com/u/61684834?v=4">
</a>
</p>



<p align="center">
Cent Bedada -
<a href="https://github.com/cent-dxv">
        <img src="https://avatars.githubusercontent.com/u/80540398?v=4">
</a>
</p>
