# Wordpress Ansible project for IT Security (2. semester)

###
Vagrant versions tested
* Vagrant 1.8.1
* Vagrant 1.7.4

Ansible versions tested:
* Ansible 2.0.1.0

Virtualization tested:
* Virtualbox v5.0 
* KVM 

####
#### About: 
When Vagrant is run, a Virtual Machine is created, it runs the Ansible playbook, which installs Apache2, PHP, MySQL and a Wordpress web app that is accessible from the LAN and a database is to be imported. 
This system will have automated Backups, so a complete restoration is done from the latest Backup after every "Vagrant up".

#### How to use:
1. Clone the repository found here: [Repository](https://github.com/Nicl0996/wordpress-ansible)
2. Make sure, Vagrant and Ansible are installed on your machine.
3. In command-line - Navigate to the Cloned repository - `cd /home/user/git/wordpress-ansible/` 
4. Start Vagrant - `vagrant up`
5. To SSH to the system - `vagrant ssh`
6. get the virtual machines ip address - `vagrant ssh-config | grep HostName | cut -d ' ' -f4`
6. To connect to Wordpress by pointing your browser to the ip addres/hostname

### Vagrantfile info:
    VM Box: debian/jessie64
    VM Provider: Virtualbox
    VM Provision: Ansible
    Ansible Playbook: "playbook.yml"

### Ansible Roles: 
    server
    apache2
    php
    mysql
    wordpress

### Pull Requests:

Before making a pull request follow the instructions in the link below.

[AboutPullRequest](https://github.com/Nicl0996/wordpress-ansible/blob/master/AboutPullRequests.md)

### Todo:
1. consolidation/basic functionality

    1. vagrant up workning with KVM and virtualbox - done
    
    2. write a basic README.md file with short description - done

    3. restructure to follow ansible best practice dir structure

    4. make script or describe how to perform integration tests

    5. describe PR requirements in reade file

    6. make vagrant up on windows work with ansible

    7. make ansible install mysql

    8. make ansible install wordpress

4. Development

    1. check_mk (not security for now)

    2. set up log server and send all logs to that server (CSC6)

    3. set up backup and restore for mysql (CSC10)

    4. set up backup and restore for wordpress (CSC10)

    5. authorized software (CSC2)

    6. secure config (CSC3) 

	
