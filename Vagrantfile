# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"
  #
  config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
    vb.memory = "4096"
  end
  config.vm.network "private_network", ip: "192.168.33.10" 
  config.vm.provision :docker
  # MAKE SURE YOU HAVE INSTALLED THE docker-compose PLUGIN!
  # vagrant plugin install vagrant-docker-compose
  
  # config.vm.synced_folder "./app", "/app"
  
  config.vm.provision :docker_compose
#  config.vm.provision "shell", inline: <<-SHELL
#    apt update
#  apt upgrade -y
#  SHELL

end
