# -*- mode: ruby -*-
# vi: set ft=ruby :

vagrant_private_ip = '192.168.50.4'

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.boot_timeout = 60

  config.vm.network "private_network", ip: vagrant_private_ip

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision/install.yml"
    ansible.host_key_checking = false
    ansible.tags = ['common', 'jenkins']
  end
end
