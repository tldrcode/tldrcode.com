Vagrant::Config.run do |config|

  config.vm.box = "trusty64-20141121"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/trusty/20141121/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.forward_port 8080, 8080

  config.vm.provision :shell,
    :inline => "sudo apt-get update && sudo apt-get -y install build-essential git ruby1.9.3 && sudo apt-get -y install nodejs ruby-bundler && sudo gem install github-pages --no-ri --no-rdoc"

  config.ssh.forward_agent = true

end
