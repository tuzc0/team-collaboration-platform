# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-24.04"
  config.vm.hostname = "Nimbus-Box"

  config.vm.boot_timeout = 600
  
  config.vm.network "private_network",
    ip: "192.168.33.30"
  
    config.vm.disk :disk,
    size: "80GB",
    primary: true
  
    config.vm.provider "virtualbox" do |vb|
    vb.name = "team-collaboration-platform"
    vb.memory = ENV.fetch("VM_MEMORY", "6144").to_i
    vb.cpus = ENV.fetch("VM_CPUS", "4").to_i
    vb.gui = false
  end

  config.vm.provision "shell",
    path: "scripts/provision.sh",
    privileged: true

end