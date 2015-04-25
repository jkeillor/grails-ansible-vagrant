
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/debian-7.6"
  
  config.vm.network :public_network, bridge: 'eth0'

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.vm.provider "virtualbox" do |vb|
  # Customize the amount of memory on the VM:
        vb.memory = "2048"
        vb.cpus = 2
  end


end

