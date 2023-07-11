Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Projeto_01_Vagrant_Shell_Script"
    vb.memory = "1024"
    vb.cpus = "1"
  end

  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8001
  config.vm.network "public_network" , ip: "192.168.0.21"
  config.vm.provision "shell", 
    inline: "apt update && apt -y install vim && apt -y install curl && apt -y install telnet && apt -y install unzip && apt -y install wget && apt -y install net-tools && apt -y install htop && apt -y install nmap && sudo useradd adenilsoncosta -s /usr/sbin/nologin"
end

