Vagrant.configure("2") do |config|
    config.vm.hostname = "elk-host"
    config.vm.provider "virtualbox" do |vb| 
        vb.memory = "1024" 
    end
    config.vm.box = "ubuntu/trusty64"
    config.vm.network :private_network, ip: "192.168.10.10" 
    config.vm.provision "ansible" do |ansible|
        ansible.playbook="elk-playbook.yml"
    end
end

