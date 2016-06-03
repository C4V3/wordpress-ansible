# Wordpress Ansible project for IT Security

### When cloning please use this command
This command will update all submodules automatically.
* `git clone --recursive URL`
* For example: `git clone --recursive https://github.com/Nicl0996/wordpress-ansible.git`

### If you didnt clone with --recursive, follow this:
* git clone URL
* cd /repository/
* git submodule init
* git submodule update

###
Vagrant versions tested
* Vagrant 1.8.1
* Vagrant 1.7.4

Ansible versions tested:
* Ansible 2.0.1.0

Virtualization tested:
* Virtualbox v5.0 
* KVM 


Getting Ansible latest Version:

* sudo apt-get install software-properties-common
* sudo apt-add-repository ppa:ansible/ansible
* sudo apt-get update
* sudo apt-get install ansible

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

### Testing the system:
Follow the instruction in the link below.

[Tests](Tests.md)

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
    generic-debian

### Generic Debian role
    This is a submodule containing an Ansible role that ensures all unattended updates are updated. 
    To add a submodule to a repository: 
   `git submodule add https://github.com/moozer/ansible-generic-debian.git generic-debian`

### Pull Requests:

Before making a pull request follow the instructions in the link below.

[AboutPullRequest](AboutPullRequests.md)

	
