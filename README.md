# 26thmay_B1_DEVOPS
## day 9
- Task 1
  ```
  Login from Mobile:
  <phoenix@192.168.1.9>
  ```
  <img src='Mobile terminal.jpeg' width='350' heidht='600'>
- Task 2
  ```
  $ vim /etc/ssh.sshd_config
  //change port = 22
  $ systemctl restart sshd.service

  //on client machine:
  shh phoenix@192.168.1.9 -p 23
  ```
  
