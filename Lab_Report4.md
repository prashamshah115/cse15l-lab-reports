# LAB REPORT 4

## TASKS TO DO: 

1. Log into ieng6
2. Clone your fork of the repository from your Github account (using the SSH URL) 
3. Run the tests, demonstrating that they fail
4. Edit the code file to fix the failing test
5. Run the tests, demonstrating that they now succeed
6. Commit and push the resulting change to your Github account (you can pick any commit message!)

## STEP 4

Keys pressed: 

`ssh<space>prs008@ieng6.ucsd.edu<enter>`

Explanation: 

The command is not run in the terminal, so we type it out including the host.

## STEP 5

Keys pressed: 

````
<open-website(https://github.com/prashamshah115/lab7)>
<click-button(<> Code)>
<click-button(copy)>
<open-terminal>
git<space>clone<space><right-click>
````

Explanation:

We first go to the github site and copy the link by clicking the copy button in the repository. Then we go to the terminal and type out the git clone commmand and use right click to paste the link that we copy from the website : `https://github.com/prashamshah115/lab7`.


## STEP 6

Keys Pressed: 

`cd<space>l<tab><enter>
bash<space>t<tab><enter>`

Explanation: 

First we will use `cd` to go into the directory we cloned. We press <tab> to auto-complete the directory name and press enter to execute. We then run the test.sh file by typing bash, and then typing t and using tab auto-complete.

## STEP 7

Keys Pressed: 

`vim<space>L<tab>.<tab><enter>
`
Explanation: 

We first use the vim command to open the vim editor for the .java file. 'L' and tab auto-complete opens ListExamples.java, then . and tab auto-complete specifies the file name to ListExamples.java instead of ListExamplesTests.java.


Keys Pressed in the vim file: 

`:set number<enter>
44gg
e
i
<delete>
2
<esc>
:x<enter>`

Explanation: 

We start off with  `:set number<enter>` to make the vim editor to display the line number. Then, we can use `44gg` to jump the cursor to line 44. Then, the `e` command moves us to the very end of the word index1, and we then change the mode to insert mode using the `i` command. Then, we delete the number 1 with `<delete>` and type the number 2 in. Finally, we save the file by changing the mode to the normal mode by pressing esc. `:x<enter>` exits.

## STEP 8

Keys Pressed: 

`bash<space>t<tab><enter>
`

Explanation: 

The bash command runs the test.sh bash script, t and tab auto-complete fills the .sh filename and the enter key is then pressed.

## STEP 9

Keys Pressed: 

`git<space>add<space>.<enter>
git<space>commit<space>-m<space>"fix<space>error"<enter>
git<space>push<enter>`

Explanation: 

git<space>add<space>.<add> adds all the files in the directory to git. Then,  git<space>commit<space>-m<space> alongside the commit "fix<space>error" and <enter> will execute the command. Lastly, we type git<space>push<enter> to push the changes to the directory to github.
