# -*- mode: ruby -*-
# # vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 8080, host: 8080

  config.vm.provision :shell,
    :inline => """sudo apt-get update && sudo apt-get -y install build-essential git ruby1.9.3 && sudo apt-get -y install nodejs ruby-bundler && cd /vagrant && sudo gem install bundler && sudo bundle install"

  config.vm.provision "jekyll", type: "shell",
    :inline => "cd /vagrant; nohup jekyll server --watch -P 8080 --force_polling > /jekyll.log &",
    run: "always"

  config.ssh.forward_agent = true

  if Vagrant.has_plugin?("vagrant-cachier")
    # Configure cached packages to be shared between instances of the same base box.
    # More info on http://fgrehm.viewdocs.io/vagrant-cachier/usage
    config.cache.scope = :box

  end
end
