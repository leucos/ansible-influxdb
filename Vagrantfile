# -*- mode: ruby -*-
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "forwarded_port", guest: 8083, host: 8083
  config.vm.network "forwarded_port", guest: 8086, host: 8086
  config.vm.network "forwarded_port", guest: 3000, host: 3000

  config.vm.provider "virtualbox" do |v|
    v.name   = "ansible-influxdb"
    v.memory = 1024
  end

  config.vm.provision "shell",
    :inline => "sudo apt-get install -y make python"

  config.vm.provision "shell",
    :path => "tests/specs.sh",
    :upload_path => "/home/ubuntu/specs",
    # change role name below
    :args => "--install ansible-influxdb"
end
