# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
# apt update and install
apt-get -qq update
# to make this error message go away:
# default: dpkg-preconfigure: unable to re-open stdin: No such file or directory
# set this environment variable DEBIAN_FRONTEND=noninteractive
DEBIAN_FRONTEND=noninteractive apt-get -qq install \
  texlive-latex-base texlive-fonts-extra ghostscript unzip
su vagrant -c '/vagrant/tengwarscript-install-guide/install-tengwar-scripts.sh'
SCRIPT

VAGRANTFILE_API_VERSION = '2'
HOSTNAME = 'elvish'
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'ubuntu/bionic64'
  config.vm.hostname = HOSTNAME
  config.vm.provider 'virtualbox' do |vb|
    vb.name = HOSTNAME
  end
  config.vm.provision 'shell', inline: $script
end
