Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "tech-test-centos7"
  config.vm.network :private_network, type: "dhcp"
  config.vm.network :forwarded_port, guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
    vb.customize ['modifyvm', :id, '--memory', 512, '--cpus', 1]
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/docker_install.yml"
    ansible.become = true
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/nginx.yml"
    ansible.become = true
  end

end