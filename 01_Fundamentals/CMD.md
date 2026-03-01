###set
 the command "set" to check your path from the command line.
 
###ver
 the "ver" command to determine the operating system (OS) version. 

### systeminfo
 the "systeminfo" command to list various information about the system such as OS information
 
###netstat
  A basic "netstat" command with no arguments will show you established connections
 -a displays all established connections and listening ports
-b shows the program associated with each listening port and established connection
-o reveals the process ID (PID) associated with the connection
-n uses a numerical form for addresses and port numbers

###dir
the child directories using "dir"
dir /a - Displays hidden and system files as well.
dir /s - Displays files in the current directory and all subdirectories.

###mkdir
create a directory, use "mkdir" directory_name; "mkdir" stands for make directory. To delete a directory, use rmdir directory_name

###type
You can easily view text files with the command "type"

###del , erase
we can delete a file using "del" or "erase".

###tasklist, tasklist
We can list the running processes using "tasklist"
 Let’s say that we want to search for tasks related to sshd.exe, we can do that with the command tasklist /FI "imagename eq sshd.exe"
Note that /FI is used to set the filter image name equals sshd.exe.

we can terminate any task using taskkill /PID target_pid. For example, if we want to kill the process with PID 4567, we would issue the command taskkill /PID 4567.

###chkdsk
chkdsk: checks the file system and disk volumes for errors and bad sectors.
driverquery: displays a list of installed device drivers.
sfc /scannow: scans system files for corruption and repairs them if possible.

we used the command more in two ways:
Display text files: more file.txt
Pipe long output to view it page by page: some_command |more
