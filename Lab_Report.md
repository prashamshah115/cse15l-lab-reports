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

The working directory when running this command was 'lecture1'. For ths command, the ouput we get is text from the terminal saying that there is no such directory as lecture1/messages/fr.txt. he 'cd' command is used to change between directories and takes the directory you wish to change to as an argument. Since the command we have passed has a file as an argument, rather than a directory, the output is as such. The output is *not* an error.

# The `ls` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ ls

*The output*

    lecture1
    [user@sahara ~]$ 

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ ls lecture1

*The output*

    Hello.class  Hello.java  messages  README
    [user@sahara ~]$ 

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~]$ ls lecture1/messages/fr.txt

*The output*

    lecture1/messages/fr.txt
    [user@sahara ~]$ 


# The `cat` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ cat

*The output*

    Blinking Cursor
    ^C // once cleared using Control C

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ cat lecture1

*The output*

    cat: lecture1: Is a directory

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~]$ cat lecture1/messages/fr.txt

*The output*

    Bonjour le Monde!
    [user@sahara ~]$ 




