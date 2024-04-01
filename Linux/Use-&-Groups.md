Tyoe of users in linux:
Type        Example     User id         Group id            Home Dir        Shell
Root        root            0               0               /root           /bin/bash   
Regular     vagrant     1000 - 60000    1000 - 60000        /vagrant        /bin/bash
Service     ftp, ssh    1 - 999          1 - 999            /var/ftp etc    /sbin/nologin
            apache   

[root@localhost ~]# useradd ansible
[root@localhost ~]# useradd jenkins
[root@localhost ~]# useradd aws

one way of adding user into group            
[root@localhost ~]# groupadd devops 
Adding group `devops' (GID 1002)  

[root@localhost ~]# usermod -aG devops ansible 
[root@localhost ~]# id ansible
uid=1000(ansible) gid=1000(ansible) groups=1000(ansible),1002(devops)
[root@localhost ~]# awk '/ansible/' /etc/group
ansible:x:1001:
devops:x:1004:ansible

Other way of adding user into the Group
sudo vim  /etc/group
devops:x:1004:ansible,aws,jenkins

# to set password to the user
[root@localhost ~]# passwd aws
Changing password for user root.
New password:
BAD PASSWORD: The password is shorter than 8 characters
Retype new password:
passwd: all authentication tokens updated successfully.

Note Reset also follow the same thing

## last command  shows the history of commands executed by a particular user. It lists up to the last 15 entries and displays each entry along with the time it[root@localhost ~]# su -l[root@localhost ~]# su -l
To check if a user has sudo access or not :
su -l username
if it asks for password then it does not have sudo access else it will show something like this :
Username=username
User ID=userid 

## [aws@localhost ~]$ lsof -u vagrant 
COMMAND   PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
sshd     1376 vagrant    3u  IPv4 159555      0t0  TCP *:22 (listen)

This means that there is a process running as 'vagrant' on port 22 which is listening to any ip address and using tcp
This means that there is a process running as 'vagrant' on port 22 which is listening to any ip address and using tcp protocol

## Deleting a user
[root@localhost ~]# userdel -r aws 
Removing home directory /home/aws.
rm: cannot remove ‘/home/aws/.bash_logout’: No such file or directory

## deleting Group
[root@localhost ~]# groupdel devops 
Group 'devops' has no members.  

## Adding users to the group using "usermod" command
usermod -aG devops aws
Adding user aws to group devops 

## Checking User and Group Membership
[root@localhost ~]# id aws
uid=1000(aws) gid=1000(aws) groups=1000(aws),1004(devops)

[root@localhost ~]# id devops
uid=1004(devops) gid=1004(devops) groups=1004(devops)

## Setting up Password aging information
[root@localhost ~]# chage -E -1 -I -1 -m 0 -M 0 -W 14 -w 14 -d 14 -aH aws
Setting password expiry date for user aws.
Warning: the values provided by chage are approximate, and the actual account age may be different. 
## Verifying Password Aging Information
[root@localhost ~]# grep ^PASS_MAX_DAYS /etc/login.defs
PASS_MAX_DAYS: 90 

The chage command in Linux is used to modify user password expiry information. Here’s a breakdown of the options you’ve provided:

-E -1: Sets the account expiration date to never expire.
-I -1: Sets the account to never be locked after the password has expired.
-m 0: Sets the minimum number of days between password changes to 0, allowing password changes at any time.
-M 0: Sets the maximum number of days between password changes to 0, which typically means the password never expires.
-W 14: Sets a warning to be issued 14 days before the password expires.
-w 14: This option is not valid; it seems like a duplicate of -W.
-d 14: Sets the number of days since January 1, 1970, when the password was last changed. However, 14 is likely incorrect as it would set the last password change to a date in early January 1970.
-aH aws: These options are not standard for the chage command. -aH does not correspond to any known chage option, and aws is not recognized in this context.