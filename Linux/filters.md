
Filter & IO Redirection

## GREP Global Regular Expression Print ####
grep firewall anaconda-ks.cfg
grep -i firewall filename -- it'll ignore the case
grep -v firewall filename -- it'll exclure the firewall

grep -i firewall * search everywherre in the current working directory
grep -iR firewall * search inside the directory as well

grep -R SELINUX /etc/* look for SELINUX in all the files and directory.

grep -c 'pattern' filename
The -c option will count the number of lines that contain the matching pattern.

grep -n 'pattern' filename
The -n option will display the line numbers along with the lines that match the pattern.

grep -w 'pattern' filename
The -w option restricts the search to whole words only.

grep -e 'pattern1' -e 'pattern2' filename
[root@localhost ~]# grep -ie user -ie password anaconda-ks.cfg
The -e option allows you to specify multiple patterns to search for in the file.


### LESS ###
less is a reader  program that displays one or more files full screen. 
can be navigated using up and down arrow.

The less command in Linux is a terminal pager program used to view the contents of a text file one screen at a time.

* Basic Usage: To open a file with less, simply type less followed by the filename:
        bash$ less filename

    Press space key to go forward and press b to go backward.
    
    q – quit (terminates the less command)
    j – move cursor down
    k – move cursor up
    g – Go to the beginning of the file.
    G – Go to the end of the file.
    /string – Search for “string” in the file.
    n – Repeat last /search.
    ESC – Exit from less (terminates the less command).

* Navigating through pages :
    When a file is too large to fit on one screen, pressing the "space" bar scrolls down one window at a time. You
    When a file is too large to fit on one screen, pressing the space bar causes it to scroll one window at a time. The amount
   
    Navigation:
        Space or f: Move forward one screen.
        b: Move backward one screen.
        Up Arrow or k: Move up one line.
        Down Arrow or j: Move down one line.
        G: Go to the end of the file.
        g: Go to the beginning of the file.
    Searching:
        /pattern: Search forward for a pattern.
        ?pattern: Search backward for a pattern.
        n: Repeat the last search forward.
        N: Repeat the last search backward.
    Other Options:
        -N: Show line numbers.
        -i: Ignore case in searches.
        -X: Leave file contents on the screen after exiting.
    Exiting:
        q: Quit less and return to the command line.


### MORE ###
More is similar to Less but it does not have some features like searching and going to specific lines. It also has fewer options compared to Less.


#### HEAD #####

head filename print the first 10 line of the file
head -20 file name prints the  first 20 lines of the file
-n number with head is used to display that many lines

#### TAIL ####

tail filename displays the last 10 lines of the file
tail -f filename will keep displaying the file as it grows, refreshing every second by default. Ctrl+C stops this.
you can use tail +number+filename, it will start displaying the file from the given line number

**Note**: In Linux/Unix systems, there are two commands named 'more' and 'less'. The main difference between them 

Note: messages are the syslog in the redhel machines

*** Every service has its own log  ***
*** keep tailing with -f that log and restarting the service , that would funnel down the error ***
