Vagrant.configure(2) do |config|
	config.vm.box = "ubuntu/xenial64"
	config.vm.network "private_network", ip: "192.168.33.10"
	config.vm.provider "virtualbox" do |vb|
		vb.memory = "2048"
	end
	config.vm.provision "shell", inline: <<-SHELL
		git clone https://github.com/patnsmith/docker-prediction-io.git
		curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
		sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
		sudo apt-get -qq update
		sudo apt-get -qq install docker-ce
		sudo curl -s -L https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
		sudo chmod +x /usr/local/bin/docker-compose
	SHELL
end
