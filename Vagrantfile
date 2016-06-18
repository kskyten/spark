# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "arch05_2016"
  config.ssh.insert_key = false
  config.vm.network "private_network", ip: "10.0.0.2"
  config.vm.provision "shell", inline: <<-SCRIPT
      echo "Updating base packages..."
      pacman --noconfirm -Syyu

      echo "Installing python2..."
      pacman -S --needed python2 --noconfirm
    SCRIPT
end
