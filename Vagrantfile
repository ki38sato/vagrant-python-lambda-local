# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
HOSTNAME1 = "vagrant-python-lambda-local"
IP1 = "192.168.200.60"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/centos-6.7"

  config.vm.define "#{HOSTNAME1}" do |guest|
    guest.vm.provision "shell", path: "ansible_local.sh"
    #guest.vm.synced_folder "/your/lambda/repository/", "/repos"
    guest.vm.network :private_network, ip: IP1
    guest.vm.hostname = "#{HOSTNAME1}"
    guest.vm.provider "virtualbox" do |vb|
      vb.name = "#{HOSTNAME1}"
    end
  end

end
