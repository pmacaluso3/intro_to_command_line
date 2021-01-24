# Intro to Command Line

## Learning Goals
1. Learn basic CLI commands
1. Use the basic commands in an exercise
1. Learn intermediate CLI commands
1. Use the intermediate commands in an exercise

## Basic Commands
#### `pwd`
This command stands for "print working directory". It tells you what directory you are standing in.

#### `ls`
This command stands for "list" and tells you what files and directories are in your current pwd. `ls` has 2 options that you need to know about:
- `ls -l` gives you extra information and an easier to read format
- `ls -a` reveals hidden files and folders. The only thing that makes a file or folder hidden is that its name starts with a dot.
- Note that you can combine the two options with `ls -la`.
- These options are called _flags_, and most commands have them. Each command uses different letters to mean different things.

#### `cd`
This command moves you into one of the directories relative to your current pwd. You have to tell this command which folder you want to move into, and specifying this folder is called giving the command an _argument_.

When using this command, it's very helpful to know about _tab completion_.

No matter where you are, you can move up by 1 directory with `cd ..`. `..` always refers to the parent directory of your current location.

#### `mv`
This command moves a file or folder somewhere else. Unlike the `cd` command that required 1 argument, the `mv` command requires 2: the file/folder to be moved, and the new destination to move it to. The 2 arguments are separated by a space. The new destination must be specified relative to your current pwd.

Note that `mv` actually does double duty: it is also the command to rename a file or folder. To rename, you use 2 arguments: the file or dir to rename, and the new name.

#### `cp`
This command copies a file or folder. It takes 2 arguments: the file or dir to copy, and the name to give the new copy.

Note that if you want to copy a directory, you need to use the `-r` flag like so:
```cp -r dir_to_copy new_name_of_dir```

#### `rm`
This removes a file or folder. Similarly to `cp`, if you want to remove a folder, you need the `-r` flag:
```rm -r dir_to_remove```.

## Navigating the mansion
Open the file `exploration.txt`. It contains challenges that you should complete on your command line. For each challenge, once you've gotten an answer that works, paste it into the `exploration.txt` under the challenge prompt. If the prompt asks you for a specific answer, like "What does the entryway contain?", put your answer to that question under the prompt as well.

In all these explorations, remember to make use of tab completion and the up arrow!

## More commands!
#### `cat`
This command takes 1 argument, the name of a file, and displays the contents of that file.

#### `echo`
This command takes 1 argument, a string, and prints that string to the terminal.

#### `>` and `>>`
These aren't actual commands but rather conjunctions. You use them to take the output of one command and write it to a file. For example: `echo Hello > hello.txt`.

The difference between `>` and `>>` is that `>` overwrites the contents of the file, and `>>` adds onto the existing contents.

#### `|`
This isn't a command, but rather a conjunction. It lets you take the output of one command and make it the input of the next command. This command is usually pronounced "pipe", as in, "run command X, and pipe its output into command Y".

#### `grep`
This command requires you to feed text into it from another command, such as `echo` or `cat`. Aside from the text that you are feeding into `grep`, it requires 1 argument of the string that you want to search for.

## Examples with intermediate commands
1. Create a file called `intermediate.txt`, and put the word `this` into it. Put the text into the file using `>`.
1. `cat` the file to see its contents.
1. Add the words `is`, `just`, `a`, `test`, `case` to the file.
1. `cat` the file to see its contents.
1. `cat` the file and pipe its contents into a `grep` command. Search for the word "test" in this file. Then try searching for other strings in it.