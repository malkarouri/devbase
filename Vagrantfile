# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/fedora-23"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.synced_folder "git/", "/opt/git"

  # Run Ansible from the Vagrant VM
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "devbase.yml"
    ansible.verbose = "vvvv"
  end
end
