Vagrant.configure("2") do |config|
  # Usar una imagen base de Ubuntu 20.04 LTS
  config.vm.box = "ubuntu/focal64"

  # Aumentar el tiempo de espera para el arranque
  config.vm.boot_timeout = 600

  # Asignar nombre a la máquina virtual
  config.vm.hostname = "servidor-prueba"

  # Configurar una IP privada
  config.vm.network "private_network", ip: "192.168.56.10"

  # Configurar la carpeta sincronizada
  config.vm.synced_folder ".", "/vagrant"

  # Provisionar con un shell script (opcional)
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get upgrade -y
  SHELL

  # Configurar la memoria de la máquina virtual
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
end


