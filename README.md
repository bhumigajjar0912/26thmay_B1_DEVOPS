# 26thmay_B1_DEVOPS

## day12
1. Task 1
```
$ mkdir /mnt/welcome
$ mount /dev/xvdf1 /mnt/welcome
```
2. Task 2
```
$ vim index (write 'HI LNB' in it)
$ cd ..
$ umount welcome
```
3. Task 3
```
Attach the volume to second/another instance
$ mkdir new
$ mount /dev/xvdf1 new
$ cd /etc/apache2/sites-available
$ vim 000-default.conf
=> Change the value of DocumentRoot to /root/new
$ cd ..
$ vim apache2.config
>>>Update as follows
<Directory />
     Options Indexes FollowSymLinks Includes ExecCGI
     AllowOverride All
     Require all granted
 </Directory>
$ sudo service apache2 restart
```
