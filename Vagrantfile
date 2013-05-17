# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu_precise_chef"

  config.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04_chef-10.18.2.box"

  config.vm.network :forwarded_port, guest: 22, host: 2277

  config.vm.network :private_network, ip: "192.168.77.10"

  # config.vm.network :hostonly, "192.168.5.10"

  config.vm.synced_folder "guest_share", "/home/host_share"


  config.vm.provider :virtualbox do |vb|
     vb.customize ["modifyvm", :id, "--memory", "1024"]
  end



end
