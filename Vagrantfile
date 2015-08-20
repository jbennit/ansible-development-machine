
# -*- mode: ruby -*-
# vi: set ft=ruby :
$script = <<SCRIPT
  ansible-playbook /u1/ansible/local-development.yml --ask-become-pass
SCRIPT
# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/vivid64"
  config.vm.network "private_network", ip: "192.168.33.40"
  config.vm.synced_folder "../ansible-development-machine", "/u1/ansible"
  config.vm.provision "shell", inline: $script
end
