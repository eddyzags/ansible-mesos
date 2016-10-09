# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "debian/jessie64"
  config.vm.network "private_network", ip: "192.168.33.7"
  config.vm.hostname = "galaxy-dev"
  config.vm.synced_folder '.', '/vagrant'

  config.vm.provider :virtualbox do |v|
    v.name = "galaxy-dev"
    v.cpus = 2
    v.customize ["modifyvm", :id, "--memory", "1024"]
  end

  # Ansible provisioning
  config.vm.provision "ansible" do |ansible|
    ansible.host_key_checking = false
    ansible.playbook = "staging"
    ansible.sudo = true
  end

end
