#vagrant init chef/centos-7.0; 
#vagrant up --provider virtualbox

# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	home_array = Dir.home.split('/')
	user = home_array[home_array.length-1]
	hostname = "nice-new-env-#{user}"

	#vagrant init puphpet/centos65-x64; vagrant up --provider virtualbox

	config.vm.hostname = hostname
	config.vm.box = "puphpet/centos65-x64"

	config.vm.network "private_network", ip: "192.168.42.106"

	config.vm.provider "virtualbox" do |vb|
		vb.memory = 512
		vb.cpus = 1
	end

	config.vm.provision "shell" do |s|
		s.path = "provisioning/setup.sh"
	end

end

