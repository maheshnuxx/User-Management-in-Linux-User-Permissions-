# User-Management-in-Linux-User-Permissions-
User Management in Linux Operating System

In Linux, User Management ensures secure multi-user access, while permissions control what each user can do with and directories. Root has Full control, regular users have limited access, and permissions(read, write, excute) define for __owners__, __groups__, and __others__.

# users in Linux
* __Root__ __User__ :- Superuser with unrestricted access. can install software, modify system files, and manage all users.
* __Regular__ __User__ :- Limited privileges, mainly for personal files and application.
* __Sudo__ __User__ :- regular User with temporary admin rights via sudo.
* __System__ __Accounts__ :- Non-human accounts used by services <br> example., <br> mysql, nginx.
* __Guest__ __User__ :- Temporary accounts with minimal privilages.
  
# user Groups
  * __Primary__ __Group__ :- Default group assigned to a user ; files created inheritsthis group.
  * __Secondary__ __Group__ :- Additional groups for extra permissions <br> example <br> developers, docker.

#command for user management:
* __useradd__ -> create a new user.
* __passwd__ -> set/change password.
* __usermod__ -> modification of user.
* __userdel__ -> user delet.

# Adding user 
* __syntax__
     * useradd {name of user} <br>
       example.,  useradd linux.

# password for user
  * __syntax__
       * passwd {name of user} <br>
         in this command for security reson passwd does not show. <br>
         for view password use ( passwd --stdin Linux ) <br>
    example., <br> __i__. passwd linux     -------does not show password. <br>
                        __[password]__ <br>
         __ii__. passwd --stdin linux    --------in this password show <br>
                        __[password]__ <br>

 # usermodication
  * __syntax__
      * usermod (modification) (username) <br>
    Example.,    useradd -aG admin linux. <br>
In this change a secondary group for user. <br>

 here are some example for user modification. <br>

 * usermod -u 1234 linux
 * usermod -G admin linux
 * usermod -c hello linux
# User Permissions in Linux 
Every file/directory has permissions for three categories: <br>

* __Owner__: The creator of the file.
* __Group__: Users in the same group.
* __Other__: All other users.

# Represntation 
 * __Symbolic__ : rwxr-xr-x --> Owner has full rights, group and others can read/execute. <br>

 * __Numerica__ : 755 --> Owner (7 = rwx), group (5 = r-x), others (5 = r-x).

 # Commands for permissions

   * ls -l  --> view permissions. <br>
   * chmod 755 filename  --> Change permissions (numeric mode). <br>
   * chmod u+x filename  --> Add execute permissions for owner (symbolic mode). <br>
   * chown user:group filename  --> Change ownership. <br>

   
     

 

             
       
