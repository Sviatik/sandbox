Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.hostname = "elk-host"
    config.vm.provider "virtualbox" do |vb| 
        vb.memory = "1024" 
    end
    config.vm.network :private_network, ip: "192.168.10.10"
    config.vm.network "forwarded_port", guest: "80", host: "8080"
    config.vm.provision "ansible" do |ansible|
        ansible.playbook="elk-playbook.yml"
    end
end

