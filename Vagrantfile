
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "debian/jessie64"
  config.vm.provider "virtualbox"
  config.vm.provision :ansible do |ansible|
   #change playbook path to whatever location it has on your own machine
   ansible.playbook = "/home/its/vagrant-prov/wordpress-ansible/playbook.yml"
  end

end
