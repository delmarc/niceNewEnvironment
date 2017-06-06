# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	home_array = Dir.home.split('/')
	user = home_array[home_array.length-1]
	hostname = "nice-new-env-#{user}"

	config.vm.hostname = hostname

	config.vm.box = "centos/7"

	config.vm.network "private_network", ip: "192.168.42.110"

	#config.vm.synced_folder '../SOMEFOLDER', '/SOMEFOLDER', nfs:true
	config.vm.synced_folder '.', '/vagrant', nfs: true
	
	config.vm.provider "virtualbox" do |vb|
		vb.memory = 2048
		vb.cpus = 1
		vb.name = "SOME-Box-Server"
	end

end

