What is sudo in linux?
 Sudo stands for "Superuser Do" and it allows users to execute commands as the super user or root. It provides a way for non-superusers

We've created a user called ansible let us go to that user and if we can execute the root comands from there

[root@localhost ~]# su - ansible
so if we run  any command it will be executed as the user "ansible" not as the superuser.

But what about this: 
bash-4.2$ sudo echo hello world
sudo: unable to initialize policy plugin
Could not receive communication

What does it mean ?

Answer: The error message you are seeing suggests that your system administrator has configured sudo to use a policy kit (pk) authentication method,
Answer: The `sudo` command allows users to temporarily assume the privileges of the superuser (usually UID 0) while executing
Answer: The `sudo` utility allows a permitted user to execute a command as the superuser or another user, as specified in the `/etc

How to add the ansible in the sudoers file 
there are two ways
1. edit the sudoers file  by using visudo or vi /etc/sudoers
    visudo
    add the user in the file
    ansible ALL=(ALL)  ALL
    wq:
    so this will add the ansible in the sudoers file and grand the root privileges but it required password to do so
    if it run sudo -i
    it'll ask for the user password
    
    to make it n uninteractive we have to supply an argument in sudoers file as below
    visudo
    ansible ALL=(ALL)   NOPASSWD: ALL
    Now you can use sudo without asking for the password.

    Note editing suduoers file is risky if  you don't know what you are doing, so always take backups of your files before making 
2. Another way of  doing it is :
    go to cd /etc/sudoers.d/
    copy the filename
    cp vagrant devops
    vim devops
    %devops	ALL=(ALL) NOPASSWD:ALL (here % used for Group)
    save & exit

    Now any user who belongs to the devops group can do sudo.


