# Command Line Basics

## Command Syntax
All commands have three parts: the **utility**, the **flags**, and the **arguments**. The utility always comes first. The other two parts have different rules, depending on which command you are using: you may not have to use any flags or arguments at all.   
Here is a sample command that you might type into a command line:

`ls -l ~/Desktop`  

Let's break this command down into parts:

- `ls` is a utility. Utilities are also sometimes known as commands all on their own, because they indicate the general idea of what you want. Most of the time, you can simply run a utility all by itself, without any flags or arguments. Most commands only have one utility.  

- `-l` is a flag that alters how the utility operates. Flags are like options or preferences: the utility will usually work perfectly well with the defaults, but sometimes, you want to modify how it works slightly. Flags always start with either one or two dashes (-), and they usually come between the utility and the arguments.  

- `~/Desktop` is an argument to the utility. Arguments are used when the utility needs to know exactly what you want for a certain action, and there is no clear default setting. You can think of it more like a conversation than an argument: The utility says "I don't know how I should do this!", and you use an argument to say, "Here, this is how you should do it." Arguments usually come at the end of the command, after the utility and the flags (if any flags are used). The number of arguments used generally depends on the utility: some don't need any arguments, some require exactly one argument, some require lots of arguments, and some are flexible in the number of arguments they can take.
This command uses the ls utility, which is used to list the contents of directories. We use the `-l` flag to indicate to the utility that we want more information than it usually provides, and so it should show us the directory contents in a long format (`-l` is short for "long"). Last, the utility wants to know, "But which directory should I list the contents of?" Using the argument, we reply, "Show me the contents of my Desktop."

In all cases, to submit a command to the computer, press enter.

## Basic Utilities
Here is a list of basic utilities that you will use on a regular basis. Anything in capital letters that starts with a dollar sign, like $THIS, is an argument to the utility. You should replace $THIS with the actual argument you want to give the computer.

- `man $UTIL`. 

**Manual**. Get information for how to use any utility. Replace $UTIL with any utility, like ls, cd, or even man! Press the up and down arrows to scroll through the documentation. Press Q to quit and go back to the command line.

- `ls $DIR`. 

**List**. Lists the contents of the directory $DIR. If no directory is specified, lists the contents of the current working directory. Use the -l flag to get more information.

- `cd $DIR`. 

**change directory**. Changes the current working directory to the directory $DIR. In effect, moves you around the computer.

- `pwd`   

**print working directory**. If you ever get lost in the computer, run this command to get a trail of breadcrumbs all the way down from the top level of the computer to see where you are.

- `less $FILE`. 

**Displays the contents of a file**. Press the up and down arrows to scroll though the file. Press Q to quit and go back to the command line.

- `cp $FILE $LOCATION`. 

**copy**. Copies the $FILE to the $LOCATION.

- `mv $FILE $LOCATION`. 

**move.** Moves the $FILE to the $LOCATION.

- `rm $FILE`. 

**remove**. Deletes a file permanently: there is no way to get it back. Be careful when using this command!

- `sudo $CMD`. 


**super user do**. When you use this utility, you use an entire command as a single argument: for example, sudo ls -l ~/Desktop. sudo asks for your user account password. As a security measure, the screen does not display anything as you type, not even asterisks (*). If the password is typed in correctly, sudo executes the $CMD with elevated permissions. Be careful when using this command!

A note about using sudo: The computer has a few built-in safety restraints to prevent normal users from doing bad things, like deleting critical files. The super user has no such restraints. Note that the super user is not necessarily bad: you must use sudo to install programs and do anything else that affects how your computer runs.

## Moving Around the Computer
Lets start by using `ls` to look around your computer. Try typing ls into the command line and pressing enter. The computer will reply with a list of names. These names are the names of files and folders in the directory you are currently in. Whenever you open up a new command line, you start in your home directory, which is the directory that generally contains all of your files.

Well, that's nice. But what if we want to go someplace else? That's what cd is for. cd requires an argument: if you tell the computer you want to go somewhere, you also have to tell it where you are going. Try entering this command:

`cd Documents`
Remember, to press enter once you have finished typing. The computer will not reply, but you are now sitting in your Documents directory. You can test this by running `ls` again: the list of names will be different.

So where do we go from here? How do we know which of these names are folders (that we can go into) and which are files (that we can't)? For that, we need more information from the `ls` command. Let's give it the `-F` flag to tell us about files and folders. Try entering this command:

`ls -F`. 

You will notice that this time, some of the names that the computer returns to you will have a slash after them. These names are folders: the rest are files. You can always `cd` into a folder by running `cd` with the folder name as an argument, as long as you can see that folder with `ls -F`.

When you're done looking in folders, it's time to go back up. But how? Luckily, every folder contains a hidden link back up. To see these hidden links, we will use the `-a` flag for ls to see all. There are at least two hidden links in every folder. The `.` (one period) link takes you back to the same folder you are currently in `—` it doesn't take you anywhere. The `..` (two periods) link takes you back up to the parent folder. In fact, you can give the `ls` command multiple flags, like so:

`ls -aF` 

If you run this command, you will notice that the . and `..` hidden links have slashes next to them, which means you can use them with cd! To go back up a folder, you can always run:

`cd ..`

Remember that if you ever get lost in the computer, you can run `pwd` to see where you are.

## Neat Tricks


- Tab Autocompletion 

 Whenever you need to type out a location in an argument (for example, in the cd command), you don't have to type out the whole thing: the first few letters will do. Once you've typed three or four letters, press the tab key, and the command line will fill in the rest for you! For example, if you are in your home directory, and you type cd Desk and then press the tab key, the command line will automatically complete the command to read cd Desktop! You can also use this if you find yourself mistyping folder names: tab autocompletion will always fill it in correctly.

- Shortcuts
  
  The command line has a few shortcuts built in. For example, to see your previously typed command, just press the up button. You can do this to submit the same command multiple times, or to edit a command that you didn't type in quite right. Another shortcut: you can use ~ (tilde) to refer to your home directory: cd ~ will take you back there.
  
# Cheat sheet

![](command-line-cheat-sheet-large02.jpg)