File Permissions
what is file permissions in linux ?
read, write and execute are the three basic actions that can be performed on a file. In Linux, these actions correspond to the following symbols:
-rwxr--r-- 1 user group  2048 Jun 30 17:59 test.txt
In the above line, what does each letter represent?
The first character indicates the type of file as follows :
d - directory
l - symbolic link
- - regular file
b - block special file
c - character special file
p - named pipe (fifo)
s - socket
u/g - owner /group
r - read permission
w - write permission
x - execute permission (only meaningful for directories and executables)
The second set of characters represents the permissions for the user who owns the file :
r – read
w – write
x – execute
The third set of characters represents the permissions for other users in the same group :
(Note that these are not shown if the group has no members.)
The fourth set of characters represents the permissions for all other users on the system :
r – read
w – write
x – execute
If any of the letters are missing, it means that the corresponding action is prohibited. For example, if rwx–r–r is
If any of these letters are missing, then that particular kind of access is prohibited. For example, if the rwx permission is displayed,
So , In the example given "test.txt" belongs to a user called 'user' and a group called 'group'. The user can read ('r'), the group can read 

-rw-r--r--  1 root root  437 Apr  1 11:52 :
-rw-------. 1 root root 2027 Jan 18 00:56 anaconda-ks.cfg
-rw-------. 1 root root 1388 Jan 18 00:56 original-ks.cfg
- => type of file
rw- => user
-r- => group
r-- => others
To change a files permission you can use chmod command. For example to make the file readable by everyone, you would run: 

let us create a directory and group as below
[root@localhost ~]# mkdir /opt/devops
[root@localhost ~]# ls /opt/
dev  devops  VBoxGuestAdditions-7.0.14
[root@localhost ~]# group devops

[root@localhost ~]# useradd aws
[root@localhost ~]# useradd ansible
[root@localhost ~]# useradd jenkins
[root@localhost ~]# useradd miles

add these users into the devops group except mile user
vim /etc/group
devops:aws.ansible,jenkins
:wq

Now check if the user is added to the Group or not by  using id command:
[root@localhost ~]# id aws
uid=1001(aws) gid=1001(aws) groups=1001(aws),1002(devops)
[root@localhost ~]# id jenkins
uid=1003(jenkins) gid=1004(jenkins) groups=1004(jenkins),1002(devops)
[root@localhost ~]# id ansible
uid=1002(ansible) gid=1003(ansible) groups=1003(ansible),1002(devops)

Now let us check the permission of created directory
[root@localhost ~]# ls -ld /opt/devops/
drwxr-xr-x 2 root root 6 Apr  3 19:17 /opt/devops/

Now change the ownership of the directory

[root@localhost ~]#  chown ansible:devops /opt/devops/
[root@localhost ~]# ls -ld /opt/devops/
drwxr-xr-x 2 ansible devops 6 Apr  3 19:17 /opt/devops/

now change the read and execute permission for group and other
[root@localhost ~]# chmod o-r /opt/devops/
[root@localhost ~]# chmod o-x /opt/devops/
add the write permission to group
[root@localhost ~]# chmod g+w /opt/devops/
Checking the permissions now :
[aws@localhost ~]$ ls -ld /opt/devops/
drwxrwx--- 2 ansible devops 6 Apr  3 19:17 /opt/devops/

Now switch to miles user
[root@localhost ~]# su - miles
[miles@localhost ~]$ ls /opt/devops/
ls: cannot open directory '/opt/devops/': Permission denied
[miles@localhost ~]$ cd /opt/devops/
-bash: cd: /opt/devops/: Permission denied

Now check with the user attached to the devops group:
[root@localhost ~]# su - aws
[aws@localhost ~]$ ls -ld /opt/devops/
drwxrwx--- 2 ansible devops 6 Apr  3 19:17 /opt/devops/
[aws@localhost ~]$ cd /opt/devops/
[aws@localhost devops]$ touch  sample.txt
[aws@localhost devops]$ ls
sample.txt

So the above conclude the permission  part, in this we have a directory named "devops" which is owned by "ansible and group is devops, if anyone other than group user wants to access the directory it'll throw permission error

There are numeric way also to change the permission

read 4
write 2
execute  1
[root@localhost ~]# chmod 770 /opt/webdata/
