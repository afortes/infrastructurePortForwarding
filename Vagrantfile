# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.ssh.insert_key = false

  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.
  config.vm.box = "centos/7"
  config.vm.define :nodoA do |op|
    op.vm.hostname = "nodeA"
    op.vm.network "private_network", ip: "10.0.0.21"
    op.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/nodeA.yml"
    end

    #op.vm.network "forwarded_port", guest: 2377, host: 2377
  end
  config.vm.define :nodoR do |op|
    op.vm.hostname = "nodoR"
    op.vm.network "private_network", ip: "10.0.0.1"
    op.vm.network "private_network", ip: "192.168.33.10"
    op.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/nodeR.yml"
    end
    #op.vm.network "forwarded_port", guest: 2377, host: 2377
  end
  config.vm.define :inet do |op|
    op.vm.hostname = "inet"
    op.vm.network "private_network", ip: "192.168.33.12"
    #op.vm.network "forwarded_port", guest: 2377, host: 2377
  end
end