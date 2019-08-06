Vagrant.configure("2") do |config|
	config.vm.define "acs" do |acs|
		acs.vm.box = "bento/ubuntu-16.04"
		acs.vm.hostname = "acs"
		acs.vm.network "private_network", ip: "192.168.33.10"
		acs.vm.provider "virtualbox" do |vb|
			vb.memory = 5048
		end
	end
	config.vm.define "web" do |web|
		web.vm.box = "centos/7"
		web.vm.hostname = "web"
		web.vm.network "private_network", ip: "192.168.33.20"
		web.vm.network "forwarded_port", guest: 80, host:8080
	end
	config.vm.define "db" do |db|
		db.vm.box = "centos/7"
		db.vm.hostname = "db"
		db.vm.network "private_network", ip: "192.168.33.30"
	end
end
