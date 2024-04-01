what is i/o redirection?
uptime > /tmp/sysinfo.txt  
cat /tmp/sysinfo.txt

free -m 
df -h
echo
echo "This script will display the uptime, free memory and disk usage information."
sleep 5 
clear

# write the output of 'free' to a file called sysinfo.txt in /tmp directory
free -m > /tmp/sysinfo.txt

# print out the contents of that file
cat /tmp/sysinfo.txt

echo
echo "Press enter to continue..."
read junk 

> for overwrite
>> for append
