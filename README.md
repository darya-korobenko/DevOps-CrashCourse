# Week 1 — Introduction into DevOps

  + [Install VirtualBox](#install-virtualBox)
  + [Install Vagrant](#install-vagrant)
  + [Using Vagrant create virtual machine with OS Linux Ubuntu 20.04](#using-vagrant-create-virtual-machine-with-os-linux-ubuntu-20.04)
  
## Install VirtualBox

1. Installed [VirtualBox](https://www.virtualbox.org/wiki/Downloads):

![VirtualBox version](/docs/virtualbox_version.png)

2. Opened VirtualBox UI:

![VirtualBox UI](/docs/virtualbox.png):

## Install Vagrant

1. Installed [Vagrant](https://developer.hashicorp.com/vagrant/downloads):

![Vagrant version](/docs/vagrant_version.png)

## Using Vagrant create virtual machine with OS Linux Ubuntu 20.04

[Vagrant documentation](https://developer.hashicorp.com/vagrant/tutorials/getting-started/getting-started-index)

1. Found [Ubuntu 20.04 Vagrant box](https://app.vagrantup.com/bento/boxes/ubuntu-20.04) and tried to install it by running:
```sh
cd C:\Users\d.korobenko\Downloads\vagrant
vagrant init bento/ubuntu-20.04
vagrant up
```
![Vagrant Error](/docs/vagrant_error.png)

2. As Vagrant threw a timeout error, searched in Stack Overflow and resolved the issue by disabling Vitual Machine Platform:

![Windows Feature](/docs/disable_feature.png)

3. Ran `vagrant up` again and VM was successfully booted:

![Vagrant up](/docs/vagrant_up.png)

4. SSH into the machine:

![Vagrant SSH](/docs/vagrant_ssh.png)

5. Opened VirtualBox UI as an admin and verified that the newly created VM is visible:

![VM Running](/docs/vm_running.png)
