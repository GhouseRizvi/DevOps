Diffrent types of files in Linux:

ls -l for long listing will give more info about the file
mkdir devopsdir
ls -l
1. - Regular file
file filename will show the types of file 
file /bin/pwd 
2. d is fordirectory
3. c is for  character file
4. b block file
5. l  is symbolic link
6. s socket file
7. p named pipe
8. S FIFO (first in first out)

creating link
mkdir -p /opt/dev/ops/devops/test
vim /opt/dev/ops/devops/test/commands.txt
    ls 
    pwd
    whoami
    cd
    uptime
    free -m
    df -h
    du -sh ./*
ls -s  /opt/dev/ops/devops/test/commands cmd

if the original file is deleted then link will be dead, if placed again link will be alive

romoving link
unlink cmd link removed original file still exists
rm -rf cmd link removes both file and link

Sorting  Files
ls -l
ls -lt shows latest first
ls -lrt show  recent first reverse
Hiding files and directories
ls -la 
. : current directory
.. : parent directory
- : hide file or directory

Changing hostname
vim /etc/hostname
 name 
 hostname devops
 log out and log back again will change the hostname.
