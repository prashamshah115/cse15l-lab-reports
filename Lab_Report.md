# PRASHAM'S LAB REPORT 

# The `cd` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ cd

*The output*

There was no output for this command.

The working directory when running this command was 'home'. We get no output for this command. The 'cd' command is used to change between directories and takes the directory you wish to change to as an argument. When no argument is provided, it takes you to the home directory but since we are already in the home directory, running this command won't give any output. The output is *not* an error. 

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ cd lecture1

*The output*

    [user@sahara ~/lecture1]$ 

The working directory when running this command was 'home'. The output we get for this command a blinking cursor, with the terminal showing us that we are now in the lecture1 directory. The 'cd' command is used to change between directories and takes the directory you wish to change to as an argument.As a result, the output of this command is to take us to the 'lecture1' directory. The output is *not* an error. 

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~/lecture1]$ cd lecture1/messages/fr.txt

*The output*

    bash: cd: lecture1/messages/fr.txt: No such file or directory
    [user@sahara ~/lecture1]$ 

The working directory when running this command was '/home/lecture1'. For this command, the ouput we get is text from the terminal saying that there is no such directory as lecture1/messages/fr.txt. The 'cd' command is used to change between directories and takes the directory you wish to change to as an argument. Since the command we have passed has a file as an argument, rather than a directory, the output is as such. The output is an error, with the error message being printed.

# The `ls` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ ls

*The output*

    lecture1
    [user@sahara ~]$ 

The working directory when running this command was 'home'. The ls command is used to print the contents of the current directory. Here, since we provide no arguments and are in the home directory, passing this command prints 'lecture1' as an output. This output is *not* an error.

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ ls lecture1

*The output*

    Hello.class  Hello.java  messages  README
    [user@sahara ~]$ 

The working directory when running this command was 'home'. The ls command is used to print the contents of the current directory. Here, since we have provided lecture1 as the directory, it prints out the names of the files in lecture1. The output is *not* an error.

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~]$ ls lecture1/messages/fr.txt

*The output*

    lecture1/messages/fr.txt
    [user@sahara ~]$ 

The working directory when running this command was 'home'. Since we have provided a filename as the argument for the command, the ls command - which prints the lists of files in the path provided in the command - obviously gives the output as shown. The output is *not* an error.


# The `cat` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ cat

*The output*

    Blinking Cursor
    ^C // once cleared using Control C

The working directory when running this command was 'home'. The cat command is used to print the contents of a file. Since we ran this command without arguments, it waits for us to input text. Whatever we type will then be displayed on the screen, and to exit, we use control + c. Hence, this output is not an error. 

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ cat lecture1

*The output*

    cat: lecture1: Is a directory

The working directory when running this command was 'home'. The cat command is used to print the contents of a file. So attempting to use this command while providing a directory name as an argument, will provide the given output since 'lecture1' is a directory and not a file. The output is *not* an error.

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~]$ cat lecture1/messages/fr.txt

*The output*

    Bonjour le Monde!
    [user@sahara ~]$ 

The working directory when running this command was 'home'. The cat command is used to print the contents of a file. Since we have provided a valid filename as an argument, the cat command prints its contents as shown. The output is *not* an error.



