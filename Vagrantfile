# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.synced_folder "./", "/vagrant"
  config.vm.provision "shell", inline: "echo hello Wordpress"

  config.vm.define :wordpress do |wordpress_config|
    wordpress_config.vm.hostname = "Wordpress"
    wordpress_config.vm.network :private_network,
      :ip => "192.168.50.10"
  end
end
