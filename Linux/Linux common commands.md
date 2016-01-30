# Linux common commands

1. Change the folder with files owner (recursive)
  
  ```
  sudo chown -R newusername /dir
  ```

2. Change permission rights for files.
  
  ```
  sudo chmod 775 filename
  sudo chmod 775 -R /dir   ##for all files in dir
  ls -l   #show file list with permissions.
  ls -la  
  ```
  
  For example access number 775 is means: 111 111 101 (-rwx-rwx-r-x). Where in each number of group 101: 1-read 0-write 1-execute. First number 7 for owner, second 7 for group, and last 5 for other users.  
  
3. Process explorer. For changing sorting column press Shift+F, choose the column name and press S, Q for quit.
  
  ```
  top
  ```
  
4. Count of CPU cores. And Linux core version

  ```
  grep -c processor /proc/cpuinfo
  uname -r
  or uname -a
  ```
  
5. Adobe Flash Player updater for Linux

  ```
  sudo apt-get install pepperflashplugin-nonfree
  sudo update-pepperflashplugin-nonfree --install
  ```
  
6. Clean aptitude cache

  ```
  sudo apt-get clean
  sudo apt-get autoclean
  sudo apt-get autoremove  
  ```  

7. Net statistic of open connections

  ```
  netstat -at4np
  lsof -i
  ```

8. Change process priority (-5 is higher priority then -1).

  ```
  sudo renice -2 -p PID
  ```
  
9. List of installed packages. If there an error with package PPA you can find and remove this from /etc/apt/sources.list.d/

  ```
  sudo dpkg --get-selections
  ```
  
10. Remove package

  ```
  sudo apt-get remove package_name
  ```

11. List of users and groups

  ```
  cat /etc/passwd
  cat /etc/group
  ```
  
12. Changing password for current user or for special user

  ```  
  passwd    ## for current user
  passwd special_username
  ```
  
13. Find lines in file by expression. And Last lines in log file

  ```
  cat /var/log/dmesg | grep .error
  last -f /var/log/dmesg
  ```
  
14. Add, delete users

  ```
  sudo userdel -r username   ##full user remove
  adduser username   #first method
  useradd -G groupname username   ##second method
  usermod -a -G groupname username  ##add user to group
  ```  

15. Shutdown PC after timer time

  ```  
  sudo shutdown -P hh:mm
  ```

16. Trace server commands

  ```
  traceroute server_address
  ping server_address
  ```

17. Archive commands

  ```
  tar -xvzf archive_file.tar
  unzip file.zip
  ```  

18. Mount and unmount devices

  ```
  lsblk  #list of devices
  mount /dev/sdb /mnt/usb0
  unmount /mnt/usb0
  
  mount -o rw,remount  ## mount root device fs system  in read/write mode in system recovery panel
  ```
