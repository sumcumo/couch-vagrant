# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
  end

   config.vm.define :couch1 do |couch_config|
    couch_config.vm.box = "sc-weatherhog/vagrant-couch"
    couch_config.vm.host_name = 'couch1.local'
    couch_config.vm.network "private_network", ip: "172.28.128.111"
    couch_config.ssh.username = "vagrant"
    couch_config.ssh.password = "vagrant" 
  end

    config.vm.define :couch2 do |couch_config|
    couch_config.vm.box = "sc-weatherhog/vagrant-couch"
    couch_config.vm.host_name = 'couch2.local'
    couch_config.vm.network "private_network", ip: "172.28.128.121"
    couch_config.ssh.username = "vagrant"
    couch_config.ssh.password = "vagrant"
  end

    config.vm.define :couch3 do |couch_config|
    couch_config.vm.box = "sc-weatherhog/vagrant-couch"
    couch_config.vm.host_name = 'couch3.local'
    couch_config.vm.network "private_network", ip: "172.28.128.131"
    couch_config.ssh.username = "vagrant"
    couch_config.ssh.password = "vagrant"
  end

end















  

