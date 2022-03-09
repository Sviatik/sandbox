Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/xenial64"
    config.vm.hostname = "elk-host"
    config.vm.provider "virtualbox" do |vb| 
        vb.memory = 4096 
        vb.cpus = 4
    end
    config.vm.network "private_network", ip: "192.168.56.10"
    config.vm.network "forwarded_port", guest: "80", host: "8080"
    config.vm.network "forwarded_port", guest: "5601", host: "5601"
    config.vm.provision "ansible" do |ansible|
        ansible.playbook="elk-playbook.yml"
    end
end

