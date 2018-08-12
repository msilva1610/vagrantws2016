# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "mrlunar/windows-server-2016-containers"
  config.vm.box_version = "2018.03.03"
  config.vm.synced_folder "D:/Arquivos/devops/vagrant/docker/ws2016", "c:/vagrant", nfs:true

  config.vm.define :dockerws2016 do |dockerws2016_config|
    # config.vm.network :forwarded_port, guest: 21, host: 21

    dockerws2016_config.vm.network :forwarded_port, guest: 8282, host: 80
    # dockerws2016_config.customize ["modifyvm", :id, "--memory", 4096]
    dockerws2016_config.vm.hostname = 'dockerws2016'
    dockerws2016_config.vm.network :private_network,
                         ip: '192.168.82.82'
    # config.vm.provision :shell, path: "boot.sh"
  end

end
