# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.define "playground" do |node|
    config.vm.network "private_network", ip: "192.168.33.100"
    config.vm.synced_folder "data", "/vagrant", create: true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook-lamp.yml"
  end
end
