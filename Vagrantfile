Vagrant.configure("2") do |config|
	config.vm.box = "ubuntu/xenial64"
	
	config.vm.network :forwarded_port, guest: 443, host: 4430, id: 'https'
	config.vm.network :forwarded_port, guest:  80, host: 8000, id: 'http'
	config.vm.network :forwarded_port, guest:  22, host: 2200, id: 'ssh'
	
	config.vm.synced_folder ".", "/vagrant", disabled: true
	config.vm.synced_folder "./", "/home/ubuntu/webroot"
end
