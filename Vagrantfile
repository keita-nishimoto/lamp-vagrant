# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "chef/centos-6.5"
  config.vm.network "private_network", ip: "192.168.33.12"
  config.vm.provider "virtualbox" do |vm|
    vm.customize ["modifyvm", :id, "--memory", "1024", "--cpus", "2", "--ioapic", "on"]
  end

  # 同階層に設置してある関連リポジトリを共有ディレクトリとしてマウント
  %w(
    playbook_lamp
  ).each do |dir|
    config.vm.synced_folder "../#{dir}", "/home/vagrant/#{dir}" if  File.exist?("../#{dir}")
  end

  config.vm.provision "ansible" do |ansible|
    ansible.limit = "all”
    ansible.inventory_path = "../playbook_lamp/hosts"
    ansible.playbook = "../playbook_lamp/site.yml"
  end
end
