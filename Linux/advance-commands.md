advance commands in linux:

Advanced linux commands are used for various administrative and system managmnet task. 
Here is the list of commands  that you should be familiar with:

1. ifconfig  - This command is used to display or configure a network interface. 
    It can also   be used to set up new interfaces.
        ifconfig
        Syntax : ifconfig [interface] [up|down]
                ifconfig [interface] hw  ether [mac-address]
                ifconfig [interface] inet_addr:[ip-address]/[subnet mask]
                         
2. netstat - This command displays network connections, routing tables, interface statistics, etc.
     The syntax of this command is as follows:
         netstat [-a] [-n] [-W] [-c] [-i | -t | -u ] 
         Here is brief explanation about options:
         -a : Show both listening and non-listening socket addresses.
         -n : Show numerical addresses instead of trying to determine symbolic host names.
         -W : In addition to showin IPv4 connections, show IPv6 connections.
         -c : Clear the kernel's connection cache.
         -i : Show information about TCP/IP protocols.
         -t : Show information about UDP protocols.
         -u : Show information about all user processes using sockets.
             
3. route - This command is used to display the routing table which contains details about how packets should be sent from one machine to another machine 
 route - This command is used to  add, delete routes to the routing table.
            Syntax : route [-n] add/del [host gw] MASK GW metric 
             Example : route add default gw  192.168.0.1 

3. top - This command provides a  live running view of a system’s resources.
       It shows tasks in order of their resource consumption.
           Syntax : top [-d delay][-n number][-b][-k][-p processID]
               -d : Delay between updates (default 5).
               -n : Number of iterations (default 5).
               -b : Use binary format for i/o amounts (default).
               -k : Showkilobytes rather than kilobits.
               -p : Process ID (PID) of one specific process.

4. ps - This command reports a snapshot of the current processes active on the system.
      Syntax : ps [options]
             Options :
             -A : Show all processes.
             -U : Display only your processes.
             -G : Display only your sessions.
             -H : High priority listing format.
             -N : Do not show any header line.
             -e : Select all processes.
             -f : Full format listing.
             -g : Group by session or job control.
             -l : Long format listing.
             -r : Show threads in a separate section from processes.
             -x : Don't display any processes which do not have an controlling terminal.

5. kill - This command is used to send specified signal(s) to the process (es) identified by pid or name. If no signal is given, SIGTERM is
5. kill - This command is used to send a signal to a specified process.
        Syntax : kill [-signal] pid ...
                kill -l [signal]
                     List all available signals.
        Signals:
               HUP INT QUIT ILL ABRT BUS FPE KILL USR1 SEGV USR2 PIPE ALRM TERM STOP CLD TSTP CONT CHLD TTIN T
                HUP INT QUIT ILL ABRT BUS FPE KILL USR1 SEGV USR2 PIPE ALRM TERM STOP
                ERR  PROF WINCH CONT CHLD TSTP TTIN TTOU URG IO XCPU XFSZ VIO

6. shutdown - This command allows  you to initiate a system shutdown and specify when it should occur.
              Syntax : shutdown [-+dhays] [time] ["message"]
                    + : Initiates immediate shutdown.
                    - : Cancels previously requested shutdown.
                    d : Initiates shutdown after 1 minute warning.
                    h : Initiates halt after 60 minutes warning.
                    y : Initiates reboot after 1 minute warning.
                    a : Aborts the system shutdown/reboot/halt request.
                    s : Stands for "system down" message.
                    The time argument specifies the date and time at which the system will be brought down, if provided. If no time is given.
                    m : Specifies the time for the shutdown/reboot/halt, if no argument given then it will be set to now
                    m : Specifies the time for the system downtime. If no argument is given, it will be set to 30 minutes.
                    The time argument specifies the date and time at which the system will be brought down, if provided. If no time argument is given
                    The time argument specifies the date and time at which the system will be shut down. If no time is given, the default is
                    The time argument specifies the date and time at which the system will be brought down, if given. If no time argument is supplied
                    The time argument specifies the date and time at which the system will be brought down.
8.   
