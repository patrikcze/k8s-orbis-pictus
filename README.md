# k8s-orbis-pictus
Playground for learning docker, kubernetes, ansible and friends

GitHub for widle!
https://desktop.github.com/

- Create Account.
- Generate SSH Keys and Import them.
- Create Empty project

VirtualBox for Widle!
https://www.virtualbox.org/wiki/Downloads

Install! 

Download : 
http://ftp.linux.cz/pub/linux/arch/iso/2019.03.01/archlinux-2019.03.01-x86_64.iso

Download Vagrant:
https://www.vagrantup.com/

Install Vagrant
Reboot Computer!


C:\HashiCorp\Vagrant\

Create Vagrant File:

# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "precise32"

    config.vm.box_url = "http://files.vagrantup.com/precise32.box"

    config.vm.network :forwarded_port, guest: 80, host: 8080
end

Run "vagrant up"

Error:
C:\Users\pnakl\Documents\GitHub\k8s-orbis-pictus>vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'precise32' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Box file was not detected as metadata. Adding it directly...
==> default: Adding box 'precise32' (v0) for provider: virtualbox
    default: Downloading: http://files.vagrantup.com/precise32.box
    default: Download redirected to host: hashicorp-files.hashicorp.com
    default:
An error occurred while downloading the remote file. The error
message, if any, is reproduced below. Please fix this error and try
again.
