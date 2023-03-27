# DevOps Crash Course Lab

by Daria Korobenko

## Week 1 — Introduction into DevOps

  + [Install VirtualBox](#install-virtualbox)
  + [Install Vagrant](#install-vagrant)
  + [Create virtual machine with OS Linux Ubuntu 20.04](#create-virtual-machine-with-os-linux-ubuntu-2004)
  
### Install VirtualBox

1. Installed [VirtualBox](https://www.virtualbox.org/wiki/Downloads):

![VirtualBox version](/docs/virtualbox_version.png)

2. Opened VirtualBox UI:

![VirtualBox UI](/docs/virtualbox.png):

### Install Vagrant

1. Installed [Vagrant](https://developer.hashicorp.com/vagrant/downloads):

![Vagrant version](/docs/vagrant_version.png)

### Create virtual machine with OS Linux Ubuntu 20.04

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

## Week 2 — Git
  
### Publish site from HTML5 UP using GitHub Pages

1. Cloned the repository locally and created a branch named develop
```sh
git clone https://github.com/darya-korobenko/DevOps-CrashCourse.git
cd C:\Users\d.korobenko\DevOps-CrashCourse
git checkout -b develop
```
2. Installed *Dimension* site template from [HTML5 UP](https://html5up.net/) and unzipped the files to DevOps-CrashCourse folder.

3. Staged the files and commited the changes:
```sh
git add html5up-dimension
git commit -m "modified main page"
```
4. Modified the header in index.html to include my initials and commited the changes:
```sh
git add index.html
git commit -m "html5up-dimension"
```
5. Pushed the branch develop into remote repository:

![Develop branch](/docs/push.png)

6. Merged the develop branch into main and pushed the changes:
```sh
git checkout main
git merge develop
git push origin main
```
7. In Github opened Settings for DevOps-CrashCourse repository and in Pages section selected the correct branch from which GitHub Pages site should be built:

![Github Pages](/docs/pages.png)

8. Verified that the site was published ([link](https://darya-korobenko.github.io/DevOps-CrashCourse/html5up-dimension/)):

![Dimension site](/docs/site.png)

9. Created a zip-archive of the site and published it as a release:

![Release](/docs/release.png)
