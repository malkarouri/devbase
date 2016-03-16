# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/fedora-23"
  config.vm.network "forwarded_port", guest: 8080, host: 8080

  # Run Ansible from the Vagrant VM
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "devbase.yml"
    ansible.verbose = "vv"
  end
end
