PROVISION = <<Script
apt-get install -y openvpn tmux
Script

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.network :private_network, ip: "10.10.10.5"
  # map local profiles directory
  config.vm.synced_folder "./profiles", "/etc/vpn_profiles/", nfs: true
  # map ssh folder to allow key access for ssh over vpn
  config.vm.synced_folder "~/.ssh", "/etc/host_ssh/", nfs: true
  config.vm.provision "shell", inline: PROVISION
end
