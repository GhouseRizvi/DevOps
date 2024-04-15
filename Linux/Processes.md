What are process in linux?
Processes in Linux are instances of executing programs. They represent individual tasks that a user can run on the system, such as web browsers, word
Processes in Linux are instances of executing programs. They represent individual tasks that a user can run on the system, such as web browsers, email.

Commands:

1. top  - This command is used to display the running processes and resources consumption on a Linux system. 

2. ps aux  – It lists all the current running processes with details such as PID, user name, CPU usage, memory usage etc.

3. ps -ef  | grep <process_name> – This command is used to list all the processes that are currently running with specific name or by using the process ID2. ps aux – It lists all the current process.

4. [root@localhost ~]# ps -ef | grep -i httpd | grep -v grep
This command will show you all the processes that have "httpd" in their name, excluding any that are part of other processes 

5. kill PID will kill the process
    [root@localhost ~]# ps -ef | grep -i httpd | grep -v grep | awk '{print $2}' | xargs kill -9

6. Commonly Used Options:
    BSD Form: ps aux
    Displays processes of all users (including those not associated with a terminal).
    Provides detailed information about the processes.
    Columns include USER, PID, %CPU, %MEM, VSZ, RSS, STAT, START, TTY, TIME, and CMD.
    UNIX Form: ps -ef
    Lists currently running processes in full format.
    Display Processes Owned by Current User: ps -x
    Lists processes owned by the current user.
    User-Oriented Format: ps -u <username>
    Lists processes for a specific user.