Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/focal64"
	config.vm.network "private_network", ip: "192.168.56.5"
	
	config.vagrant.plugins = "vagrant-docker-compose"
	
	config.vm.provision :docker
	config.vm.provision :docker_compose
	
	
	config.vm.provider :virtualbox do |vb|
		vb.name = "enter name here"
	end
	config.vm.provider "virtualbox" do |v|
        v.memory = 4096
        v.cpus = 2
		v.customize ["modifyvm", :id, "--groups", "/Vagrant"]
    end
end