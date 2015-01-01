Vagrant::Config.run do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.forward_port 8080, 8080

  config.vm.provision :shell,
    :inline => """sudo apt-get update && sudo apt-get -y install build-essential git ruby1.9.3 && sudo apt-get -y install nodejs ruby-bundler && cd /vagrant && sudo gem install bundler && sudo bundle install"

  config.vm.provision "jekyll", type: "shell",
    :inline => "cd /vagrant; nohup jekyll server --watch -P 8080 --force_polling > /jekyll.log &",
    run: "always"

  config.ssh.forward_agent = true

end
