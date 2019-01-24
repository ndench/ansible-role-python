# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = 'ubuntu/xenial64'

  config.vm.network "private_network", type: "dhcp"
  config.vm.synced_folder "./", "/etc/ansible/roles/ndench.python"

  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.galaxy_role_file = "tests/requirements.yml"
    ansible.playbook = "tests/main.yml"
    ansible.verbose = 'vv'
    ansible.become = true
  end
end
