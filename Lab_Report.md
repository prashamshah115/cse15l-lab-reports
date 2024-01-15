# PRASHAM'S LAB REPORT 

# The `cd` command

## An example of the command with no arguments

*The command*

    [user@sahara ~]$ cd

*The output*

There was no output for this command.

## An example of the command with a path to a directory as an argument.

*The command*

    [user@sahara ~]$ cd lecture1

*The output*

    [user@sahara ~/lecture1]$ 

## An example of using the command with a path to a file as an argument.

*The command*

    [user@sahara ~/lecture1]$ cd lecture1/messages/fr.txt

*The output*

    bash: cd: lecture1/messages/fr.txt: No such file or directory
    [user@sahara ~/lecture1]$ 

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




