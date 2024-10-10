# Linux File-Directory Administration
Using Linux commands, we are able to change file/directory permissions for particular users. This lab is meant to demonstrate my personal ability and comfortability with some of these operations. <br />
Note: This is being performed within a controlled lab environment with a network admin account "researcher2@f3a9c23ffbf9".

<br />

<h2>Checking file and directory details</h2>
First thing we need to do is navigate to our desired file in our directory. We can move to a specific directory folder with the "cd" (change directory) command. <br />
We can then list files in the current directory with the "ls" command. 
Adding the "-la" flags puts the list in "long format" (-l) and also includes any "hidden" files or directories available (-a). 
<br /> <br />
<img src="https://i.imgur.com/hYpqKqF.png" height="80%" alt="Check file and directory details"/>
Notice the 10-character "permission string" of file: project_k.txt = -rw-rw-rw- <br />
This indicates that in this file, the User, Group, and Other role assignments are all able to read (r) and write (w) on this file, but not execute (x).


<br />
<br />
<br />


<h2>Changing file permissions</h2>
Using the "chmod" (change mode) command, we can edit the permissions of a particular group. 
<br /> <br /> 
<img src="https://i.imgur.com/LQClkxj.png" height="80%" alt="Change file permissions"/>
In this example, we removed the "write" (w) permission from the Other (o) group. <br /> 
Alternatively, if we wanted to ADD the write permission to the same group, we would instead enter "chmod o+w".


<br />
<br />
<br />


<h2>Change file permissions on a hidden file</h2>
We can also edit the file permission of any "hidden" file or directories that would not appear under a normal list display.
<br /> <br />
<img src="https://i.imgur.com/ing3ERK.png" height="80%" alt="Change file permissions on a hidden file"/>
In this step, we changed the "user" and "group" roles to only be able to read the hidden file ".project_x.txt". <br />
While not explicitely shown here, without the "-a" flag included in the list command, no files beginning with "." would be displayed.


<br />
<br />
<br />



<h2>Change directory permissions</h2>
Lastly, we change the permissions of the "drafts" directory so that only the "user" role has any type of access to it. <br />
This is done in the same way that it would be done for any other type of file.
<br /> <br />
<img src="https://i.imgur.com/bihkmZg.png" height="80%" alt="Change directory permissions"/>
It should be noted that only directories display a "d" at the beginning of their permission strings.


<br />
<br />
<br />



<h2>Summary:</h2>
The goals of this Lab were as follows: <br />
● View/identify “projects” directory permissions (including hidden files)<br />
● Remove other’s write access to any file<br />
● Change hidden file permissions, so user/group to only read access<br />
● Change ‘drafts’ directory to only allow user access
