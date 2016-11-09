# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
  end

   config.vm.define :couch1 do |couch_config|
    couch_config.vm.box = "hor"
    couch_config.vm.host_name = 'couch1.local'
    config.vm.network "public_network", type: "dhcp"
  end

    config.vm.define :couch2 do |couch_config|
    couch_config.vm.box = "hor"
    couch_config.vm.host_name = 'couch2.local'
    config.vm.network "public_network", type: "dhcp"
  end

    config.vm.define :couch3 do |couch_config|
    couch_config.vm.box = "hor"
    couch_config.vm.host_name = 'couch3.local'
    config.vm.network "public_network", type: "dhcp"
  end

end















  

