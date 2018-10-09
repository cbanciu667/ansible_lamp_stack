
$script_sed = <<SCRIPT
echo "Replace sshd_conf line"
sed -i 's/PasswordAuthentication\ no/PasswordAuthentication\ yes/g' /etc/ssh/sshd_config
sed -i 's/AuthorizedKeysFile/#AuthorizedKeysFile/g' /etc/ssh/sshd_config
sudo systemctl restart sshd
echo "Done".
SCRIPT

#VM configuration

Vagrant.configure("2") do |config|


  config.vm.box = "debian/stretch64"
  config.vm.network "private_network", ip: "10.0.0.2"
  config.vm.provision "shell", inline: $script_sed
#  config.vm.provision "shell", inline: $script_jenkins
  config.vm.provider "virtualbox" do |vm|
        vm.name = "ubuntu18lts"
  			vm.customize [
  							'modifyvm', :id,
  							'--memory', '2048'

  						]
  end
end
