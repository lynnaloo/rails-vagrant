
## Creating a Vagrant Virtual Development Environment for Ruby Development ##

[Vagrant](http://docs.vagrantup.com/v2/why-vagrant/index.html) is open-source software used to create lightweight
and portable virtual development environments. Vagrant works like a "wrapper" for VirtualBox that can create,
configure, and destroy virtual machines with the use of its own terminal commands. Vagrant facilitates the setup
of environments without any direct interaction with VirtualBox and allows developers to use preferred editors
and browsers in their native operating system.

Note: This document is for setting up a virtual environment on a Unix host.

###  Install Vagrant ###

- Download and install [VirtualBox 4.3.12](https://www.virtualbox.org/wiki/downloads)
  - Do not open VirtualBox or create a virtual machine. This will be handled by Vagrant.
- Download and install [Vagrant 1.6.3](http://www.vagrantup.com/downloads.html)
  - Package managers like apt-get and gem install will install an older version of Vagrant so it is required to use the download page.

### Install VirtualBox Guest Additions Plugin

    host $ vagrant plugin install vagrant-vbguest

### Connect to the Virtual Machine ###

Start the virtual machine:

    host $ vagrant up

Connect to the virtual machine via ssh:

    host $ vagrant ssh

Bundle the Ruby gems:

    vagrant $ cd dev
    vagrant $ bundle install
