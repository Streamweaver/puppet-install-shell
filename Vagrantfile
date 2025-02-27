# -*- mode: ruby -*-
# vi: set ft=ruby :

if Vagrant::VERSION < '1.5.0'
  fail 'This Vagrantfile uses Vagrantcloud, upgrade to > 1.5.0!'
end

Vagrant.configure("2") do |config|

   # Want to make sure cachier doesn't give false positives
  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.auto_detect = false
  end

  config.vm.define "centos_362" do |centos_362|
    centos_362.vm.box = 'centos6.5'
    centos_362.vm..box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-65-x64-virtualbox-nocm.box"
    centos_362.vm.provision "shell", path: "install_puppet.sh", args: "-v 3.6.2"
    centos_362.vm.provision "shell", inline: "puppet --version"
  end

  # Test for facter issue from https://github.com/petems/vagrant-puppet-install/issues/6
  config.vm.define "GH6" do |gh6|
    gh6.vm.box = "chef/ubuntu-12.04-i386"
    gh6.vm.provision "shell", path: "install_puppet.sh", args: "-v 2.7.23 -fv 1.7.6"
    gh6.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "GH6_centos" do |gh6_centos|
    gh6_centos.vm.box = "chef/centos-6.5"
    gh6_centos.vm.provision "shell", path: "install_puppet.sh", args: "-v 2.7.23 -fv 1.7.6"
    gh6_centos.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "centos510" do |centos510|
    centos510.vm.box = "chef/centos-5.10"
    centos510.vm.provision "shell", path: "install_puppet.sh"
    centos510.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "centos65" do |centos65|
    centos65.vm.box = "chef/centos-6.5"
    centos65.vm.provision "shell", path: "install_puppet.sh"
    centos65.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "centos7" do |centos65|
    centos65.vm.box = "chef/centos-7.0"
  end

  config.vm.define "precise64" do |precise64|
    precise64.vm.box = "chef/ubuntu-12.04"
    precise64.vm.provision "shell", path: "install_puppet.sh"
    precise64.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "quantal64" do |quantal64|
    quantal64.vm.box = "chef/ubuntu-12.10"
    quantal64.vm.provision "shell", path: "install_puppet.sh"
    quantal64.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "raring64" do |raring64|
    raring64.vm.box = "chef/ubuntu-13.04"
    raring64.vm.provision "shell", path: "install_puppet.sh"
    raring64.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "saucy64" do |saucy64|
    saucy64.vm.box = "chef/ubuntu-13.10"
    saucy64.vm.provision "shell", path: "install_puppet.sh"
    saucy64.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "trusty64" do |trusty64|
    trusty64.vm.box = "chef/ubuntu-14.04"
    trusty64.vm.provision "shell", path: "install_puppet.sh"
    trusty64.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "squeeze" do |squeeze|
    squeeze.vm.box = "chef/debian-6.0.8"
    squeeze.vm.provision "shell", path: "install_puppet.sh"
    squeeze.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "wheezy" do |wheezy|
    wheezy.vm.box = "chef/debian-7.4"
    wheezy.vm.provision "shell", path: "install_puppet.sh"
    wheezy.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "fedora19" do |fedora19|
    fedora19.vm.box = "chef/fedora-19"
    fedora19.vm.provision "shell", path: "install_puppet.sh"
    fedora19.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "fedora20" do |fedora20|
    fedora20.vm.box = "chef/fedora-20"
    fedora20.vm.provision "shell", path: "install_puppet.sh"
    fedora20.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "fedora21" do |fedora20|
    fedora20.vm.box = "chef/fedora-21"
    fedora20.vm.provision "shell", path: "install_puppet.sh"
    fedora20.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "arch" do |arch|
    arch.vm.box = "losingkeys/arch"
    arch.vm.provision "shell", path: "install_puppet.sh"
    arch.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "freebsd9" do |freebsd9|
    freebsd9.ssh.shell = 'sh'
    freebsd9.vm.guest = :freebsd
    freebsd9.vm.box = "chef/freebsd-9.2"
    freebsd9.vm.provision "shell", path: "install_puppet.sh"
    freebsd9.vm.provision "shell", inline: "puppet --version"
  end

  config.vm.define "freebsd10" do |freebsd10|
    freebsd10.ssh.shell = 'sh'
    freebsd10.vm.guest = :freebsd
    freebsd10.vm.box = "chef/freebsd-10.0"
    freebsd10.vm.provision "shell", path: "install_puppet.sh"
    freebsd10.vm.provision "shell", inline: "puppet --version"
  end

end
