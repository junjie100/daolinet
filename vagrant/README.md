This page includes instructions for building your own demo system
=================================================================

Prerequisites:
--------------
The host you are using to build the demo system should have the following prerequisites:
* Install VirtualBox 4.3.32 or greater
* Install Vagrant 1.7.4
* In order to run the demo smoothly, your host should have 4-core CPU with 4G RAM

Installation Requirements:
--------------------------
Before install the Virtualbox, these tools are necessary:

    % sudo yum install -y kernel-devel kernel-headers kernel gcc

Reboot your machine:

    % sudo reboot

Get Virtualbox repo:

    % wget -P /etc/yum.repos.d http://download.virtualbox.org/virtualbox/rpm/{distro}/virtualbox.repo
  
Replace {distro} with your Linux distribution (eg: el for CentOS, rhel for Red Hat, fedora for Fedora).


Install the Virtualbox:

    $ sudo yum install -y VirtualBox-5.0.x86_64


Install the Vagrant:

    $ sudo rpm -ivh https://releases.hashicorp.com/vagrant/1.7.4/vagrant_1.7.4_x86_64.rpm


Running:
--------
In current directory.

    % ./pre.sh
    % vagrant ssh

Visit our system by 10.10.10.10. The login id is "admin", login password is "daolinet", and the instance password is "daoli123".
If you have stopped and restarted the instance, wait for 30 seconds then testing connectivity.

Deleting:
---------
In current directory. 

    % vagrant destroy
