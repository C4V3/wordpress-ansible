# Wordpress Ansible project for IT Security (2. semester)
#### About: 
When Vagrant is run, a Virtual Machine is created, it runs the Ansible playbook, which installs Apache2, PHP, MySQL and a Wordpress web app that is accessible from the LAN and a database is be imported. This system has automated Backups, so a complete restoration is done from the latest Backup after every "Vagrant up".

#### How to use:
1. Clone the repository found here: [Repository](https://github.com/Nicl0996/wordpress-ansible)
2. Make sure, Vagrant and Ansible are installed on your machine.
3. In command-line - Navigate to the Cloned repository - `cd /home/user/git/wordpress-ansible/` 
4. Start Vagrant - `vagrant up`
5. To SSH to the system - `vagrant ssh`
6. To connect to Wordpress - `vagrant ssh `

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

### Tasks:
	- Clean up - done
	- Vagrant up working - done
	- Install Apache 2 - done
	- Install MySQL
	- Install Wordpress
	- Write a ReadMe file
	- Backup Wordpress
	- Backup MySQL


	
