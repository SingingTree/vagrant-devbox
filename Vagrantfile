Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.hostname = "singingtree-linux-devbox"
  config.vm.network "private_network", type: "dhcp"

  config.vm.provision :salt do |salt|
    salt.masterless = true
    salt.install_type = "stable"
    salt.minion_config = "saltstack/etc/minion"
    salt.run_highstate = true
  end
end