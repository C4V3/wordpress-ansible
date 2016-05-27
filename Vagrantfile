VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # set up provisioners
  config.vm.provider :libvirt do |libvirt|
    libvirt.host = ""
    libvirt.nested = false
    libvirt.memory = 1024
  end

  config.vm.provider :virtualbox do |virtualbox|
    virtualbox.network "public_network",
      use_dhcp_assigned_default_route: true
  end


  # setup servers
  config.vm.box = "debian/jessie64"
  servers = ['webserver', 
             'logserver',
             'moniserver']
  
  servers.each do |hostname|
    config.vm.define "#{hostname}" do |node|
      node.vm.hostname = "#{hostname}"
    end
  end

  # provisioning
  config.vm.provision :ansible do |ansible|
   ansible.playbook = "playbook.yml"
  end
end  
