
Grep: 

grep "81.143.211.90" access.log

## **Searching Recursively with grep**
For example, to search for a variable across **all files** in the current directory and its subfolders, we can run:

```bash
grep -R "PRETTY_NAME" /etc/
```

**What is SSH & how Does it Work?**

- SSH allows us to remotely execute commands on another device remotely.
- Any data sent between the devices is encrypted when it is sent over a network such as the Internet

![[Pasted image 20260124230131.png]]

For example: `ssh tryhackme@MACHINE_IP`


**Introduction to Flags and Switches**

ls -a 

ls --help

File System Commands:

touch <filename>. -> Create an empty file

**Switching Between Users**

Switching between users on a Linux install is performed using command 'Su'


Common Directories

**/etc**
The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system. 

For example, the sudoers file highlighted in the screenshot below contains a list of the users & groups that have permission to run sudo or a set of commands as the root user.

**/var**

The "/var" directory, with "var" being short for variable data. This folder stores data that is frequently accessed or written by services or applications running on the system. For example, log files from running services and applications are written here (**/var/log**),

/**root**

 the **/root** folder is actually the home for the "root" system user.
 
**/tmp**

This is a unique root directory found on a Linux install.

General/Useful Utilities

**Downloading Files (Wget)**

wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt

**Transferring Files From Your Host - SCP (SSH)**

Secure copy, or SCP, is just that -- a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using the SSH protocol to provide both authentication and encryption.

scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt

**Serving Files From Your Host - WEB**

python3 -m  http.server

**Processes 101**

**Viewing Processes**

To see the processes run by other users and those that don't run from a session (i.e. system processes)

ps aux

**Managing Processes**

You can send signals that terminate processes; there are a variety of types of signals that correlate to exactly how "cleanly" the process is dealt with by the kernel.

To kill a command, we can use the appropriately named `kill` command and the associated PID that we wish to kill. i.e., to kill PID 1337, we'd use `kill 1337`.

Below are some of the signals that we can send to a process when it is killed:

- SIGTERM - Kill the process, but allow it to do some cleanup tasks beforehand
- SIGKILL - Kill the process - doesn't do any cleanup after the fact
- SIGSTOP - Stop/suspend a proces

**How do Processes Start?**

Let's start off by talking about namespaces. The Operating System (OS) uses namespaces to ultimately split up the resources available on the computer to (such as CPU, RAM and priority) processes.

Namespaces are great for security as it is a way of isolating processes from another -- only those that are in the same namespace will be able to see each other.

 **Getting Processes/Services to Start on Boot**
For example, to tell apache to start up, we'll use `systemctl start apache2`

We can do four options with `systemctl`:

- Start
- Stop
- Enable
- Disable