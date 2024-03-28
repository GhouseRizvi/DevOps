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
             
3. route - This command is used to display the routing table which contains details about how packets should be sent from one machine to another 
