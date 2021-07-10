1)	top:  this command is used to know the cpu utilization in Linux .
` top`
2)	How to list top/last ‘5’ cpu utilization processes?
``` 
ps –auxf | sort –nr –k 3 | head –5
ps –auxf | sort –nr –k 3 | tail  –5
```
3)	How to replace a string in a file? Stream editor sed
```
sed –i “s/<old string>/<new String>/g”  <filename>
Eg:  sed –i “s/unix/linux/g” /root/Desktop/language.txt
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
8)	How to copy a file from windows to unix?
10)	List  all the files and directories in a directory?
11)	List all the hidden files in a directory?
12)	How to list all the files in ling list format?
13)	How to list all the running java processes?
14)	How to list all the listening ports ?
15)	How to know the port number based on process id<PID>?
16)	How to know the processed id <PID> based on port number?
17)	How to change the file permissions?
18)	What is the use of sticky bit?
19)	Command to go to previous directory?
20)	Command to go to root User directory?
21)	Command to check ip address?
22)	Command to check free disk space?
23)	Command to find free memory?
24)	How to change ownership of a file?
25)	How to find how many users are logged in that unix box?
26)	How to find with which user name is logged in?
27)	How to find the given OS is 32 bit or 64 bit?
28)	How to find the given os version?
29)	I want to execute a script, everyday at 5:00pm. 	Write a  crontab syntax to achieve that?
