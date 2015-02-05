# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

			
	config.vm.define :trail do |trail|
		trail.vm.hostname = "com.paxce"
		trail.vm.box = "ubuntu"
		trail.vm.box_url = "https://dl.dropboxusercontent.com/s/r5okkx8330h3tzh/vagrant-centos-5.10-x86_64.box"
						
		trail.vm.network :private_network, ip: "192.168.111.2"
						
		trail.vm.provision "puppet" do |trail|
		trail.manifests_path = "../manifests"
		trail.manifest_file = "../manifests/1.pp"
		trail.module_path = "../modules"
		end		
		
			
				
		trail.vm.provider "virtualbox" do |prov|
				prov.customize ["modifyvm", :id, "--memory", "512"]
				prov.customize ["modifyvm", :id, "--cpuexecutioncap", "30"]
							end
	
end
end
