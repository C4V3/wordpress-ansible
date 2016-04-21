# Requirements
A machine running linux is required, use a virtual machine if needed.
You need ansible installed. Do "apt-get install ansible", may need to be root.

# Forking and cloning the repository
Go to https://github.com/nicl0996/wordpress-ansible and press fork in the upper right corner. Login if needed.
Create a local clone from the forked repository using
"git clone https://github.com/YOUR-USERNAME/wordpress-ansible". Replace YOUR-USERNAME with your own github account username.

# Running the playbook
Go into the directory of the files. For example "cd /home/jesper/wordpress-ansible
Edit the hosts file to either localhost or the ip address of the server(can be the machine you are working on) with "nano hosts"
Change the hostfile location to "/home/USER/wordpress-ansible". Swap USER with your username.
Generate public/private key pairs with "ssh-keygen". Press enter through all the steps.
Copy the public key from the localhost (can be the same virtual machine) with "ssh-copy-id IP-ADDRESS". Replace IP-ADDRESS with the ip of the server.
Run it with ansible using "ansible-playbook playbook.yml -i hosts -u USER -k" Replace user with the name of your user

# Error solving
If you have sudo problems install sudo and add the relevant access to the user in /etc/sudoers.
Go into /etc/ansible/ansible.cfg, uncomment ask_sudo_pass and set it to = Yes