require "yaml"

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network :private_network, ip: "10.0.0.200"
  config.ssh.forward_agent = true

  config.vm.provider :virtualbox do |v|
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--memory", 2048]
    v.customize ["modifyvm", :id, "--name", "machine"]
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "80"]
    v.cpus = 2
  end
end
