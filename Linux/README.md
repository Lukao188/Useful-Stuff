1)	top:  this command is used to know the cpu utilization in Linux .
```
top
```
2)	How to list top/last ‘5’ cpu utilization processes?
``` 
ps -auxf | sort -nr -k 3 | head -5   # For ps command 'a' show processes for all users, 'u' display the process's user/owner, 'x' also show processes not attached to a terminal, 'f' Displays a full listing
ps -auxf | sort -nr -k 3 | tail -5   # For sort command 'n' numeric sort in 'r' reverse order '-k 3' collumn 3 or CPU value
```
3)	How to replace a string in a file? Stream editor sed
```
sed -i “s/<old string>/<new String>/g”  <filename>
Eg:  sed -i “s/unix/linux/g” /root/Desktop/language.txt
```
4)	How to copy a file within box?
```
cp  <file1>  <file2>   # copy file1 to file 2 within the directory.
cp  <file1>  /tmp      # copy file1 to /tmp directory with same name.
cp  <file1>  ~raj      # copy file1 to Home directory of raj.
```
5)	How to copy a file from one unix box to another unix box?
```
scp <filename1> <username>@<ip address or hostname>:<path where to copy>
Eg:  scp sample.txt rajkumar@192.168.32.64:/root/Desktop/raj    # Copy file sample.txt to 192.168.32.64 box /root/Desktop/raj directory.
```
6)	How to copy a file from unix to windows?
```
ftp <ip address>
ftp> <username>
ftp> <password>
ftp>cd ../../../..                          # move to particular directory to copy file)
ftp> put  <filename>  /dir                  # put is used to copy a file to unix box  a particular directry
ftp> mput <file1> <file2> …<file n> /dir    # put multiple files to unix box a particular dir.
ftp> get <filename>                         # get a file from unix box to windows.
ftp> mget <file1> <file2> ..<file n>        # get multiple file from unix box to windows
ftp> quit                                   # used to quit from unix box.
```
7)	How to copy a file from windows to unix? WINSCP, MobaXterm, X–Manager, Reflection –X…. etc.
8)	List  all the files and directories in a directory?
```
ls       # list all the files and directories in within directory
ls -a    # list all the hidden files in a directory
ls -l    # list files in a long list format, with permissions, '-' indicates files, 'd' indicates directory
ls -ltr  # sort by modification time in reverse order, oldest entries will be shown first
```
9)	How to list all the running java processes?
```
ps -ef | grep java  # '-e' means select all processes and '-f' in full format
```
10)	How to list all the listening ports ?
```
netstat -a
```
11) How to know the port number based on process id or port number?
```
netstat  -antp | grep <pid>   # Based on pid. In netstat '-a' all, '-n' show ip instead of host names, '-t' show only tcp connections, '-p' show process id/name
netstat  -antp | grep <port>  # Based on port number
```
12)	How to change the file permissions?
```
chmod ugo+rwx <filename>  # give read, write, and execute to ugo: current user, group user, other user
chmod 777 <filename>      # give read write executable to everyone
```
13)	Command to go to directory?
```
cd -  # previous
cd ~  # users home directory
```
14)	Command to check ip address?
```
ifconfig
```
15)	Command to check free disk space?
```
df -h           # Shows the amount of disk space used and available on Linux file systems in human readable format
du -sh /<path>  # Report only the total disk space occupied by a directory tree and to suppress subdirectories
```
16)	Command to find free memory?
```
free -m   # In '-m' megabytes
vmstat    # Used memory (statistics)
```
17)	How to change ownership of a file?
```
chown  <user name>:<group name>  <file name>
chown -R <user name>:<group name> <Path of the directory>  # Recursively change for the entire directory
```
18)	How to find how many users are logged in that unix box? 
```
users
who
```
