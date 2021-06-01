# 26thmay_B1_DEVOPS

## day 6
- Task 1
  ```
  sudo adduser test
  sudo su test
  cd Desktop
  ```
- Task 2
  ```
  sudo groupadd lnb
  mkdir welcome
  sudo chgrp lnb welcome
  ```
- Task 3
  ```
  sudo useradd -m u1
  sudo useradd -m u2
  sudo useradd -m u3
  sudo usermod -aG lnb u1
  sudo usermod -aG lnb u2
  sudo usermod -aG lnb u3
  ```
- Task 4
  ```
  chmod 774 welcome/
  ```
