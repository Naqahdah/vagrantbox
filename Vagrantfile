# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "xubuntu"
  config.vm.network "private_network", ip: "192.168.50.10"
  config.vm.network "forwarded_port", guest: 80, host: 8888
  config.vm.hostname = "xubuntubox"
  config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 4
  end
end