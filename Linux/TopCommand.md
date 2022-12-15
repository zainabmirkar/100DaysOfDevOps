## Top Command (table of processes)

![image](https://user-images.githubusercontent.com/85761276/207924084-257a7489-1753-480a-be4a-a7f81019d491.png)

- top command is used to show the Linux processes. It provides a dynamic real-time view of the running system.
-  Usually, this command shows the summary information of the system and the list of processes or threads which are currently managed by the Linux Kernel. 

![image](https://user-images.githubusercontent.com/85761276/207924295-4c0489f5-347d-4ec1-91d0-167c09de2348.png)

- Exit Top Command After Specific repetition: Top output keep refreshing until you press ‘q‘. 
- With below command top command will automatically exit after 2 number of repetition.

![image](https://user-images.githubusercontent.com/85761276/207926184-aa76b7dc-fa51-4fef-9c84-7d2772ecad45.png)
- Specific user process
 top -u paras
 
 Press ‘z‘ option in running top command will display running process in color which may help you to identified running process easily Z 
- Shows Absolute Path of Processes: Press ‘c‘ option in running top command, it will display absolute path of running pro Z 
- Kill running process: You can kill a process after finding PID of process by pressing ‘k‘ option in running top command without exiting from top window as shown below. 
- Sort by CPU Utilisation: Press (Shift+P) to sort processes as per CPU utilization. 
- Shows top command syntax:

- secure mode : top -s

## How to view the entire list of processes?

- ps(process status) : report a snapshot of the current processes.

## pgrep
- The pgrep command is used to find out the PIDs of a running program based on different criteria.
- allows you to user regular expressions

![image](https://user-images.githubusercontent.com/85761276/207931436-90c14e68-9450-4913-8052-00befc021fc3.png) <br/>
If there are running processes with names matching “init”, their PIDs will be displayed on the screen. If no matches are found, the output is empty.

## Difference between top and ps
- top allows you display of process statistics continuously until stopped vs. ps which gives you a single snapshot.
- top is like a task manager

### Reference 
https://www.geeksforgeeks.org/top-command-in-linux-with-examples/ <br/>
https://linuxize.com/post/pgrep-command-in-linux/
