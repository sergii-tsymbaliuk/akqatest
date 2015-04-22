# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "akqatesttask.vm.local"
  
  config.vm.network :private_network, ip: "192.168.56.101"
  config.ssh.username = 'vagrant'
  config.ssh.password = 'vagrant'  
  config.ssh.forward_agent = true 
  
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |vb|
	vb.customize ["modifyvm", :id, "--hwvirtex", "on"]
    vb.customize ["modifyvm", :id, "--cpus", 1]
    vb.gui = false
    vb.memory = "512"
  end
  
  config.vm.provision "docker" do |docker|
    docker.pull_images "ser9ey/testapp"
	docker.run "ser9ey/testapp",
		args: "-i -t -d -p '0.0.0.0:80:80'"
  end
  
end
