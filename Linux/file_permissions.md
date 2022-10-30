
to add new user : sudo adduser zun  <br/>


chown: <br/>
change ownership for that newuser: sudo chown zun newfile.txt <br/>


![image](https://user-images.githubusercontent.com/85761276/197486657-c062bc36-d4f2-4360-93b5-a4f504843f03.png)


chmod:<br/>

Another way to use chmod is to provide the permissions you wish to give to the owner, group, and others as a three-digit number. The leftmost digit represents the<br/>permissions for the owner.<br/> The middle digit represents the permissions for the group members. The rightmost digit represents the permissions for the others.
<br/>
The digits you can use and what they represent are listed here:<br/>

0: (000) No permission.<br/>
1: (001) Execute permission.<br/>
2: (010) Write permission.<br/>
3: (011) Write and execute permissions.<br/>
4: (100) Read permission.<br/>
5: (101) Read and execute permissions.<br/>
6: (110) Read and write permissions.<br/>
7: (111) Read, write, and execute permissions.<br/>

# Advanced File Permisions:
- Access control list (ACL) provides an additional, more flexible permission mechanism for file systems.
- For each file, getfacl displays the file name, owner, the group, and the ACL (Access Control List). <br/>

   ![image](https://user-images.githubusercontent.com/85761276/198867813-2edf03b8-a233-459f-8b7b-c30458a39801.png)
   
- setfacl sets (replaces), modifies, or removes the access control list (ACL) to regular files and directories. <br/>
- zainab has no permission for creating a file in testing directory. By setfacl permission is easily set. <br/>
    
   ![image](https://user-images.githubusercontent.com/85761276/198868165-a85aed14-3add-4232-b60d-c9935dc84bb4.png)

- setfacl for groups <br/>
   ![image](https://user-images.githubusercontent.com/85761276/198868575-05e10a13-a342-4dc5-9280-ab7230605d77.png)

- -m is for modifying, -x is for removing <br/>

<br/>
References:
https://www.howtogeek.com/437958/how-to-use-the-chmod-command-on-linux/  <br/>
https://www.youtube.com/watch?v=wBp0Rb-ZJak&t=6578s <br/>
https://www.youtube.com/watch?v=U-vPg-xGXi4  <br/>
https://github.com/bregman-arie/devops-exercises/tree/master/topics/linux#questions-linux-permissions <br/>
https://www.geeksforgeeks.org/access-control-listsacl-linux/
