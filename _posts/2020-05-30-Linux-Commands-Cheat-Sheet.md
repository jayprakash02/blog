---
layout: post
title:  "Linux Commands List"
date:   2021-05-30 21:15:19 +0530
categories: Linux
author: Jay prakash
---

### Hardware Information

#### Show bootup messages:

{% highlight ruby %}
dmesg
{% endhighlight %}

#### See CPU information:

{% highlight ruby %}
cat /proc/cpuinfo
{% endhighlight %}

#### Display free and used memory with:

{% highlight ruby %}
free -h
{% endhighlight %}

#### List hardware configuration information:

{% highlight ruby %}
lshw
{% endhighlight %}

#### See information about block devices:

{% highlight ruby %}
lsblk
{% endhighlight %}

#### Show PCI devices in a tree-like diagram:

{% highlight ruby %}
lspci -tv
{% endhighlight %}

#### Display USB devices in a tree-like diagram:

{% highlight ruby %}
lsusb -tv
{% endhighlight %}

#### Show hardware information from the BIOS:

{% highlight ruby %}
dmidecode
{% endhighlight %}

#### Display disk data information:

{% highlight ruby %}
hdparm -i /dev/disk
{% endhighlight %}

#### Conduct a read-speed test on device/disk:

{% highlight ruby %}
hdparm -tT /dev/[device]
{% endhighlight %}

#### Test for unreadable blocks on device/disk:

{% highlight ruby %}
badblocks -s /dev/[device]
```

### Searching

#### Search for a specific pattern in a file with:

{% highlight ruby %}
grep [pattern] [file_name]
{% endhighlight %}

#### Recursively search for a pattern in a directory:

{% highlight ruby %}
grep -r [pattern] [directory_name]
{% endhighlight %}

#### Find all files and directories related to a particular name:

{% highlight ruby %}
locate [name]
{% endhighlight %}

#### List names that begin with a specified character [a] in a specified location [/folder/location] by using the find command:

{% highlight ruby %}
find [/folder/location] -name [a]
{% endhighlight %}

#### See files larger than a specified size [+100M] in a folder:

{% highlight ruby %}
find [/folder/location] -size [+100M]
```

### File Commands

#### List files in the directory:

{% highlight ruby %}
ls
{% endhighlight %}

#### List all files (shows hidden files):

{% highlight ruby %}
ls -a
{% endhighlight %}

#### Show directory you are currently working in:

{% highlight ruby %}
pwd
{% endhighlight %}

#### Create a new directory:

{% highlight ruby %}
mkdir [directory]
{% endhighlight %}

#### Remove a file:

{% highlight ruby %}
rm [file_name] 
{% endhighlight %}

#### Remove a directory recursively:

{% highlight ruby %}
rm -r [directory_name]
{% endhighlight %}

#### Recursively remove a directory without requiring confirmation:

{% highlight ruby %}
rm -rf [directory_name]
{% endhighlight %}

#### Copy the contents of one file to another file:

{% highlight ruby %}
cp [file_name1] [file_name2]
{% endhighlight %}

#### Recursively copy the contents of one file to a second file:

{% highlight ruby %}
cp -r [directory_name1] [directory_name2]
{% endhighlight %}

#### Rename [file_name1] to [file_name2] with the command:

{% highlight ruby %}
mv [file_name1] [file_name2]
{% endhighlight %}

#### Create a symbolic link to a file:

{% highlight ruby %}
ln -s /path/to/[file_name] [link_name]
{% endhighlight %}

#### Create a new file:

{% highlight ruby %}
touch [file_name]
{% endhighlight %}

#### Show the contents of a file:

{% highlight ruby %}
more [file_name]
{% endhighlight %}

#### or use the cat command:

{% highlight ruby %}
cat [file_name]
{% endhighlight %}

#### Append file contents to another file:

{% highlight ruby %}
cat [file_name1] >> [file_name2]
{% endhighlight %}

#### Display the first 10 lines of a file with:

{% highlight ruby %}
head [file_name]
{% endhighlight %}

#### Show the last 10 lines of a file:

{% highlight ruby %}
tail [file_name]
{% endhighlight %}

#### Encrypt a file:

{% highlight ruby %}
gpg -c [file_name]
{% endhighlight %}

#### Decrypt a file:

{% highlight ruby %}
gpg [file_name.gpg]
```
#### Show the number of words, lines, and bytes in a file:
```
wc
```
### Directory Navigation

#### Move up one level in the directory tree structure:

{% highlight ruby %}
cd ..
{% endhighlight %}

#### Change directory to $HOME:

{% highlight ruby %}
cd
{% endhighlight %}

#### Change location to a specified directory:

{% highlight ruby %}
cd /chosen/directory
```

### File Compression

#### Archive an existing file:

{% highlight ruby %}
tar cf [compressed_file.tar] [file_name]
{% endhighlight %}

#### Extract an archived file:

{% highlight ruby %}
tar xf [compressed_file.tar]
{% endhighlight %}

#### Create a gzip compressed tar file by running:

{% highlight ruby %}
tar czf [compressed_file.tar.gz]
{% endhighlight %}

#### Compress a file with the .gz extension:

{% highlight ruby %}
gzip [file_name]
```

### File Transfer

#### Copy a file to a server directory securely:

{% highlight ruby %}
scp [file_name.txt] [server/tmp]
{% endhighlight %}

#### Synchronize the contents of a directory with a backup directory using the rsync command:

{% highlight ruby %}
rsync -a [/your/directory] [/backup/] 
```

### Users

#### See details about the active users:

{% highlight ruby %}
id
{% endhighlight %}

#### Show last system logins:

{% highlight ruby %}
last
{% endhighlight %}

#### Display who is currently logged into the system with the who command:

{% highlight ruby %}
who
{% endhighlight %}

#### Show which users are logged in and their activity:

{% highlight ruby %}
w
{% endhighlight %}

#### Add a new group by typing:

{% highlight ruby %}
groupadd [group_name]
{% endhighlight %}

#### Add a new user:

{% highlight ruby %}
adduser [user_name]
{% endhighlight %}

#### Add a user to a group:

{% highlight ruby %}
usermod -aG [group_name] [user_name]
{% endhighlight %}

#### Temporarily elevate user privileges to superuser or root using the sudo command:

{% highlight ruby %}
sudo [command_to_be_executed_as_superuser]
{% endhighlight %}

#### Delete a user:

{% highlight ruby %}
userdel [user_name] 
{% endhighlight %}

#### Modify user information with:

{% highlight ruby %}
usermod
```
Process Related


#### See a snapshot of active processes:

{% highlight ruby %}
ps
{% endhighlight %}

#### Show processes in a tree-like diagram:

{% highlight ruby %}
pstree
{% endhighlight %}

#### Display a memory usage map of processes:

{% highlight ruby %}
pmap
{% endhighlight %}

#### See all running processes:

{% highlight ruby %}
top
{% endhighlight %}

#### Terminate a Linux process under a given ID:

{% highlight ruby %}
kill [process_id]
{% endhighlight %}

#### Terminate a process under a specific name:

{% highlight ruby %}
pkill [proc_name]
{% endhighlight %}

#### Terminate all processes labelled “proc”:

{% highlight ruby %}
killall [proc_name]
{% endhighlight %}

#### List and resume stopped jobs in the background:

{% highlight ruby %}
bg
{% endhighlight %}

#### Bring the most recently suspended job to the foreground:

{% highlight ruby %}
fg
{% endhighlight %}

#### Bring a particular job to the foreground:

{% highlight ruby %}
fg [job]
{% endhighlight %}

#### List files opened by running processes:

{% highlight ruby %}
lsof
{% endhighlight %}

#### Show system information:

{% highlight ruby %}
uname -r 
{% endhighlight %}

#### See kernel release information:

{% highlight ruby %}
uname -a  
{% endhighlight %}

#### Display how long the system has been running, including load average:

{% highlight ruby %}
uptime 
{% endhighlight %}

#### See system hostname:

{% highlight ruby %}
hostname
{% endhighlight %}

#### Show the IP address of the system:

{% highlight ruby %}
hostname -i 
{% endhighlight %}

#### List system reboot history:

{% highlight ruby %}
last reboot 
{% endhighlight %}

#### See current time and date:

{% highlight ruby %}
date
{% endhighlight %}

#### Query and change the system clock with:

{% highlight ruby %}
timedatectl 
{% endhighlight %}

#### Show current calendar (month and day):

{% highlight ruby %}
cal
{% endhighlight %}

#### List logged in users:

{% highlight ruby %}
w
{% endhighlight %}

#### See which user you are using:

{% highlight ruby %}
whoami
{% endhighlight %}

#### Show information about a particular user:

{% highlight ruby %}
finger [username]
```

### Disk Usage

##### You can use the df and du commands to check disk space in Linux.


#### See free and used space on mounted systems:

{% highlight ruby %}
df -h
{% endhighlight %}

#### Show free inodes on mounted filesystems:

{% highlight ruby %}
df -i
{% endhighlight %}

#### Display disk partitions, sizes, and types with the command:

{% highlight ruby %}
fdisk -l
{% endhighlight %}

#### See disk usage for all files and directory:

{% highlight ruby %}
du -ah
{% endhighlight %}

#### Show disk usage of the directory you are currently in:

{% highlight ruby %}
du -sh
{% endhighlight %}

#### Display target mount point for all filesystem:

{% highlight ruby %}
findmnt
{% endhighlight %}

#### Mount a device:

{% highlight ruby %}
mount [device_path] [mount_point]
```
### SSH Login


#### Connect to host as user:

{% highlight ruby %}
ssh user@host
{% endhighlight %}

#### Securely connect to host via SSH default port 22:

{% highlight ruby %}
ssh host
{% endhighlight %}

#### Connect to host using a particular port:

{% highlight ruby %}
ssh -p [port] user@host
{% endhighlight %}

#### Connect to host via telnet default port 23:

{% highlight ruby %}
telnet host
```
### Chown command in Linux changes file and directory ownership.


#### Assign read, write, and execute permission to everyone:

{% highlight ruby %}
chmod 777 [file_name]
{% endhighlight %}

#### Give read, write, and execute permission to owner, and read and execute permission to group and others:

{% highlight ruby %}
chmod 755 [file_name]
{% endhighlight %}

#### Assign full permission to owner, and read and write permission to group and others:

{% highlight ruby %}
chmod 766 [file_name]
{% endhighlight %}

#### Change the ownership of a file:

{% highlight ruby %}
chown [user] [file_name]
{% endhighlight %}

#### Change the owner and group ownership of a file:

{% highlight ruby %}
chown [user]:[```group] [file_name]
{% endhighlight %}

#### List IP addresses and network interfaces:

{% highlight ruby %}
ip addr show
{% endhighlight %}

#### Assign an IP address to interface eth0:

{% highlight ruby %}
ip address add [IP_address]
{% endhighlight %}

#### Display IP addresses of all network interfaces with:

{% highlight ruby %}
ifconfig
{% endhighlight %}

#### See active (listening) ports with the netstat command:

{% highlight ruby %}
netstat -pnltu
{% endhighlight %}

#### Show tcp and udp ports and their programs:

{% highlight ruby %}
netstat -nutlp
{% endhighlight %}

#### Display more information about a domain:

{% highlight ruby %}
whois [domain]
{% endhighlight %}

#### Show DNS information about a domain using the dig command:

{% highlight ruby %}
dig [domain] 
{% endhighlight %}

#### Do a reverse lookup on domain:

{% highlight ruby %}
dig -x host
{% endhighlight %}

#### Do reverse lookup of an IP address:

{% highlight ruby %}
dig -x [ip_address]
{% endhighlight %}

#### Perform an IP lookup for a domain:

{% highlight ruby %}
host [domain]
{% endhighlight %}

#### Show the local IP address:

{% highlight ruby %}
hostname -I
{% endhighlight %}

#### Download a file from a domain using the wget command:

{% highlight ruby %}
wget [file_name]
```
### Linux Keyboard Shortcuts


#### Kill process running in the terminal:

{% highlight ruby %}
Ctrl + C
{% endhighlight %}

#### Stop current process:

{% highlight ruby %}
Ctrl + Z
{% endhighlight %}

##### The process can be resumed in the foreground with fg or in the background with bg.



#### Cut one word before the cursor and add it to clipboard:

{% highlight ruby %}
Ctrl + W
{% endhighlight %}

#### Cut part of the line before the cursor and add it to clipboard:

{% highlight ruby %}
Ctrl + U
{% endhighlight %}

#### Cut part of the line after the cursor and add it to clipboard:

{% highlight ruby %}
Ctrl + K
{% endhighlight %}

#### Paste from clipboard:

{% highlight ruby %}
Ctrl + Y
{% endhighlight %}

#### Recall last command that matches the provided characters:

{% highlight ruby %}
Ctrl + R
{% endhighlight %}

#### Run the previously recalled command:

{% highlight ruby %}
Ctrl + O
{% endhighlight %}

#### Exit command history without running a command:

{% highlight ruby %}
Ctrl + G
{% endhighlight %}

#### Run the last command again:

{% highlight ruby %}
!!
{% endhighlight %}

#### Log out of current session:

{% highlight ruby %}
exit
{% endhighlight %}
