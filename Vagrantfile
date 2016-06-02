VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.define "webserver" do |webserver|
    webserver.vm.network "public_network",
      use_dhcp_assigned_default_route: true
    webserver.vm.box = "debian/jessie64"
    webserver.vm.hostname = "webserver"
    webserver.vm.provider "virtualbox"
    webserver.vm.provision :ansible do |ansible|
     ansible.playbook = "playbook.yml" 
    end 
  end

  config.vm.define "logserver" do |logserver|
    logserver.vm.network "public_network",
      use_dhcp_assigned_default_route: true
    logserver.vm.box = "debian/jessie64"
    logserver.vm.hostname = "logserver"
    logserver.vm.provider "virtualbox"
    logserver.vm.provision :ansible do |ansible|
     ansible.playbook = "playbook.yml"
    end
  end

  config.vm.define "moniserv" do |moniserv|
    moniserv.vm.network "public_network",
      use_dhcp_assigned_default_route: true
    moniserv.vm.box = "debian/jessie64"
    moniserv.vm.hostname = "moniserv"
    moniserv.vm.provider "virtualbox"
    moniserv.vm.provision :ansible do |ansible|
     ansible.playbook = "playbook.yml"
    end
  end

end  
