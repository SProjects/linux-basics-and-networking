# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
 
  config.vm.define "bats" do |bats|
    bats.vm.box = "ubuntu/trusty64"
    bats.vm.hostname = "bat"
    bats.vm.network "private_network", ip: "192.168.33.10"
    bats.vm.synced_folder "linux-unix-basics/", "/home/vagrant/linux/"
  end

end