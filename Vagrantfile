VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "debian/jessie64"
  config.vm.provider "virtualbox"
  #config.vm.synced_folder "/home/its/vagrant-prov/wordpress-ansible", "/home/vagrant/wordpress-ansible", type: "rsync"
  #config.vm.provision :shell, :path "ansibleinst.sh"}
  config.vm.provision :ansible do |ansible|
   ansible.playbook = "/home/morten/anble/wordpress-ansible/playbook.yml"
   #ansible.inventory_path = "/home/its/vagrant-prov/wordpress-ansible/hosts"
  end

end