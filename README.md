# 26thmay_B1_DEVOPS

## day 11
1. Create a dir 'new' at mnt

```
$ mkdir /mnt/new
```
2. Create a folder and attach to EC2 instance

```
Attach by selecting the volume and Clicking 'Attach Volume'
Then Select the instance in which you want to attach

To see the voume in terminal
$ fdisk -l
```
3. Creating and mounting partition
  - Creating partition
    ```
    $ fdisk /dev/
    Welcome to fdisk (util-linux 2.34).
    Changes will remain in memory only, until you decide to write them.
    Be careful before using the write command.


    Command (m for help): n
    Partition type
    p   primary (2 primary, 1 extended, 1 free)
    l   logical (numbered from 5)
    Select (default p):

    Using default response p.
    Selected partition 4
    First sector (4147200-10485759, default 4147200):
    Last sector, +/-sectors or +/-size{K,M,G,T,P} (4147200-10485759, default 10485759): +1.5G

    Created a new partition 4 of type 'Linux' and of size 1.5 GiB.

    Command (m for help):w
    ```
  - Mounting partition
    ```
    $ mount /dev/xvdf1 /mnt/new
    ```
4. Install Apache web server
```
$ sudo apt install apache2
```
5. Changing root dir
```
$ cd /etc/apache2/sites-available
$ vim 000-default.conf
=> Change the value of DocumentRoot to /mnt/new
$ cd ..
$ vim apache2.config
>>>Update as follows
 <Directory />
     Options Indexes FollowSymLinks
     AllowOverride All
     Require all denied
 </Directory>
$ sudo service apache2 restart
```
