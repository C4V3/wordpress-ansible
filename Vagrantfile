VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "debian/jessie64"
  config.vm.provider "virtualbox"
  config.vm.provision :ansible do |ansible|
   ansible.playbook = "playbook.yml"
   
  end

end