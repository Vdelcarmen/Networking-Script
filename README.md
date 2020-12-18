# Networking-Script

In this assignment we're trying to store important network information and storing that information in a file called NetworkDump

# CentOS:  In order for this file to work, the user must be root. 12.14.20_Networking will send output to /root/NetworkDump
hostname    -------The hostname command displays thr current name of the Server

ifconfig | grep inet | head -1   ------- The ifconfig command displays network information but when used with grep we can target "inet" which display the ip address

netstat -tulpn | grep listen     ------- The netstat command displays network connections in this case we are using some options -tulpn,  t will display TCP ports, u will display UDP ports, l will display listening ports, p displays the program, n display the port number. 

yum history   -------The Yum history command displays all the updates made to the system, it’s a powerful tool for monitoring system and package updates                

df -h    -----The df command gives us the amount of free space in all file systems, in this case we see the root file system current has 15 Gigabits of free space, the -h gives the storage in a human readable format

ls /etc/yum.repos.d    ------Yum.repos.d directory contains all the installed repositores, repositories are package installation points

uname -sv     -------To get Kernel information we can use uname -sv, -s option gives us the name of the kernel while the -v option display the version of said kernel

yum history   ------Yum history display all the updates and installaton of programs

# Ubuntu:   In order for this file to work, the user must be root. 12.14.20_Networking_ubuntu will send output to /root/NetworkDump
hostname

ifconfig

cat resolv.conf

netstat -tulpn | grep LISTEN

cat /var/log/dpkg.log | grep -e "installed" -e "20-12-14"   ------ To get the update history we can view a file called dpkg.log in the /var/log directory

df -h

-------
We can check for reps in /etc/apt/sources/list.d directory and the etc/apt/sources.list file. If we travel to the /etc/apt/sources.list.d we can see installed repositories, here we can see the PPA repository we installed to update vim.

ls /etc/apt/sources.list.d
cat /etc/apt/sources.list | grep ^[^#]  


uname -sv
