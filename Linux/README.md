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
19)	How to find with which user name is logged in?
```
whoami
who am i 
```
20)	How to find the given OS is 32 bit or 64 bit?
```
arch
uname -m
```
21)	How to find the given os version?
```
more /etc/*release
```
22)	Crontab syntax?
```
* * * * * <path of script>  # minute (0-59), hour (0-23), day of month (1-31), month (1-12), day of week (0-6) Sunday 0 or 7
crontab –l                  # list all cronjobs on your system
less /etc/crontab           # display contents of the root user’s crontab
```
23)	What is the difference between kill –3, kill –9 and kill –15?
```
kill -3 <PID>    # to generate the “Thread dumps”
kill -9 <PID>    # to kill the process forcibly
kill -15 <PID>   # it will wait to kill the process until the child processes are killed
```
24)	What is the command to make/extract a tar file?
```
tar -cvf <filename>.tar <path of the desired folder>   # '-c' create an archive file, '-v' show the progress of the archive file, '-f' filename of the archive file
tar -xvf <filename>.tar /<directory to extract>        # '-x' extract an archive file
```
25)	What is the difference between tail and head commands?
```
head    # lists the top files
tail    # lists the last files
```
26)	How to add a new user and change it's password?
```
useradd <user name>
passwd <new password>
```
27)	How to check the connectivity between two unix boxes?
```
ping <ip address>
```
28)	What is the difference between find and grep command?
```
find . -name “<filename>”    # searches recursively in current directory
find / -name “<filename>”    # searches recursively all the directories in file system
find ~/ -name “<filename>”   # searches recursively the root directory

grep “<string>”	<filename>   # searches the word in a particular file, but it is not recursive
```
29)	How to check Webserver is running or not?
```
ps  auxf | grep httpd
```
30)	How to run a process in the background? Put  “& “ at the end of the command.
31)	How to bring the process to foreground?
```
fg  <pid>
```
32)	Command to find files which are older than 15 days?
```
find <directory path> -atime +15	   # find {directory to search in}  –atime  {+ greater than, – less than, without anything means equal to}  {number of days}
atime   # file access time shows the last time the data from a file was accessed 
ctime   # change time changes when you change file's ownership or access permissions
mtime   # modify time shows time of the  last change to file's contents
```
33)	Command to find recent modified files?
```
ls -lrt
```
34)	What is the use of umask and what is the default umask value? The umask specifies the permissions you do not want given by default to newly created files and directories. Default umask value is 022.
35)	How to mount a file system?
```
mount <file system name> <where to mount>    # A file system can be "mounted" on your Linux system interactively or automatically at startup. Then the file system is just as accessible as any other file system on your computer.
Eg: mount/dev/cdrom /mnt/cdrom
umount <file system name>                    # Command to "detach" a mounted file or directory 
```
36) Command  to find top 5 files which consumes high disk usage?
```
du -sm *|sort -nr | head -5       # Here ‘s’ summarizes all the reports, ‘m’ indicates size in MB.
```
37)	What is the command to find the files size more than 100 MB?
```
find . -size +100M    # In current directory
find /<dirname> -size +100M
```
38)	What is the use of lsof command? Lsof stands for list the open files, which will list all the open files in the system (including network connection, devices and directories).
39)	What is the difference between softlink and hardlink?
```
softlink     # create a separate inode for linked file. We should not delete the original file to access the softlink.
hardlink     # It doesn’t have a separate inode. Hard link file will be deleted when we delete the original file.
```
40)	What are different run levels in Linux?
```
Run  Level 0: Halt System (To shutdown the system)
Run Level 1: Single user mode
Run Level 2: Basic multi user mode without NFS
Run Level 3: Full multi user mode (text based)
Run Level 4: unused
Run Level 5: Multi user mode with Graphical User Interface
Run Level 6: Reboot System
```
41)	Command to find HOSTNAME of system?
```
hostname
```
42)	Command to display number of lines in a file?
```
wc -l <filemname>   # number of lines in a file
wc -m <filename>    # number of characters in a file
wc -w <filename>    # number of words in a file
wc <file name>      # number of lines ,words and bytes in a given file
```
43)	Command to list number of files in a directory?
```
ls -l <directory> |  wc  -l
```
