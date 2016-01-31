# Ansible installation

1. Change the folder with files owner (recursive)
  
  ```
  sudo apt-get install software-properties-common
  sudo apt-add-repository ppa:ansible/ansible
  sudo apt-get update
  sudo apt-get install ansible
  ```
2. Instructions for another platforms - [http://docs.ansible.com/intro_installation.html#installation](http://docs.ansible.com/intro_installation.html#installation)

3. Check version.

  ```
  ansible --version
  ```
