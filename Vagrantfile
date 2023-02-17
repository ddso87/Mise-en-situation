# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Configuration de la machine virtuelle "app"
  config.vm.define "app" do |app|
    app.vm.box = "ubuntu/focal64"
    app.vm.hostname = "app"
    app.vm.network "private_network", ip: "172.16.8.11"
    app.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
	
    app.vm.provision "shell", inline: "mkdir -p ~/.ssh"
    app.vm.provision "shell", inline: "chmod 700 ~/.ssh"
    app.vm.provision "shell", inline: "echo 'ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC0rQBHezDKOf7kEnm4MPpAgvD7PZZgM+ScA3qfJ2hl5GMtvW6aifhbtgwwP1lBeTp8JLhvULlo2t29l3BysF2owPVh8r6ySYAtHNWXAjQJWuR9QK9V8L7by1Mbm3PoCvpO56DWrs/osAtl1LtTJqV5N7a0lmh7h1Yv9pzZFIJrhcOly6ZdmzY8mNyTAYB08WYEP/7QvuyphWWh08tkiOphVbFLXBcfA3hWkIzHM6Dy/g2iE48vW1AU720t5xv6bD4Tq+F52EGZa16WnYlARnO0hYS9lgG+kpbX1Rm4MmL87QwwNcUbG0xlIlSUJGTW1h5iCpyuhLF5ehRIb0oILI2f9fdj7CSf68YNCsvFHGCHzR2YRoH71LfdlyIV/Liyox4sH6hGrkrCyDydGJ/oCXHjlIWr1irDVEeG+TIJnJAYNiQiDXSahKoa1nTbp1xhKNXCuY/OSe5m5NBoct18Hr3YrtswshJAEYeKjIdD12W7v3R7U+kgKTlPbdPvJbdaon8k8WaT8sQdGPdviaWpRzrCQrKtzGWLov7aCrAjuYcyb39Xyffo0VgWMaVNRAfDB7Iq4zHscuWY1R4i/281TCUYi5LBBDEFtezZFS6AfxjeExQH3U0ENndWPaceEnxujv05lRNHyHY3jKrf4ZbMSOdyppKWToqXobLefm9v3Bn/fw== admin@Vagrant
' > ~/.ssh/authorized_keys"
    app.vm.provision "shell", inline: "chmod 600 ~/.ssh/authorized_keys"
  end

  # Configuration de la machine virtuelle "web"
  config.vm.define "web" do |web|
    web.vm.box = "ubuntu/focal64"
    web.vm.hostname = "web"
    web.vm.network "private_network", ip: "172.16.8.12"
    web.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end

  # Configuration de la machine virtuelle "backup"
  config.vm.define "backup" do |backup|
    backup.vm.box = "ubuntu/focal64"
    backup.vm.hostname = "backup"
    backup.vm.network "private_network", ip: "172.16.8.13"
    backup.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end
  end

end
