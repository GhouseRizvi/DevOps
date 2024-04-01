What is awk in linux:
<s>awk is a powerful tool for processing or filtering text files. It allows you to manipulate data by applying rules based on patterns matched within
 vim info.txt
    fristName       lastName        age     city       ID
    Thomas          Shelby          30      Rio        400
    Omega           Night           45      Ontario    600
    Wood            Tinker          54      Lisbon     N/A
    Giorgos         Georgiou        35      London     300
    Timmy           Turner          32      Berlin     N/A

to print all the content of the file , you can use this command :  
awk '{print}'  info.txt

to print the specific column:
awk '{print $4}' info.txt
To get a line that contains 'Turner' and to list only the city column,you can use this command:
awk '$2 ~ /Turner/{print $4}' info.txt

How to print out lines with a specific pattern in awk
awk '/^O/' information.txt [ ^ indicate the begining of the line]
This will print out any lines starting with "O".

[vagrant@localhost ~]$ awk '/^O/' info.txt
Omega           Night           45      Ontario    600
[vagrant@localhost ~]$ awk '/0$/' info.txt
Thomas          Shelby          30      Rio        400
Omega           Night           45      Ontario    600
Giorgos         Georgiou        35      London     300

awk '!/0$/' info.txt
This will print out any lines not ending with zero.
[vagrant@localhost ~]$ awk '!/0$/' info.txt
fristName       lastName        age     city       ID

Wood            Tinker          54      Lisbon     N/A
Timmy           Turner          32      Berlin     N/A


You can also combine patterns using && or || . For example:

awk '/^O/&&!/0$/' info.txt
This prints out lines starting with "O" but not ending with zero.

How to use regular expressions in awk
If you want to look for words containing io, you'd do:
[vagrant@localhost ~]$ awk '/io/{print $0}' info.txt
Thomas          Shelby          30      Rio        400
Omega           Night           45      Ontario    600
Giorgos         Georgiou        35      London     300

[vagrant@localhost ~]$ awk '/IT/' info.txt
Thomas          Shelby          30      Rio        400  IT
Wood            Tinker          54      Lisbon     N/A  IT

see only the first and last names of the people working in IT?
[vagrant@localhost ~]$ awk '/IT/{print $1,$2}' info.txt
Thomas Shelby
Wood Tinker

find lines that end with the pattern N/A.
[vagrant@localhost ~]$ awk '/N\/A/' info.txt
Wood            Tinker          54      Lisbon     N/A  IT
Timmy           Turner          32      Berlin     N/A  Engineering

How to use comparisson operators in awk:
-eq, -ne, -lt, -le, -gt, -ge : These are used for numeric comparison.
==, != : These are used for string comparison.

Let’s say we wanted to find all the people who work in IT and have an age greater than 30:

[vagrant@localhost ~]$ awk '/IT/&&$3>30' info.txt
Thomas          Shelby          30      Rio        400  IT
Wood            Tinker          54      Lisbon     N/A  IT</s>

[vagrant@localhost ~]$ awk '/IT/ && $3 -ge 30' info.txt
Thomas          Shelby          30      Rio        400  IT
Wood            Tinker          54      Lisbon     N/A  IT
You can also mix conditions together like this:

[vagrant@localhost ~]$ awk '($3 > 30) && ($4 < 500)' info.txt
Thomas          Shelby          30      Rio        400  IT  

[vagrant@localhost ~]$ awk '$3 - ge 30 /IT/' info.txt
Thomas Shelby 30 Rio 400 IT
Wood Tinker 54 Lisbon N/A IT    
