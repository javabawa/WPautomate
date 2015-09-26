# WPautomate
Automated setup of a production WP environment on Ubuntu 14.4.3

The objective of this exercise is to create a set of automation scripts that will setup a full Wordpress product environement on DigitalOcean (DO). I need to do this for a WP+WooCommerce store i want to setup.

After reading a number of articles on WP automation, I've concluded that a combo of Ansible and WP CLI is ideal for small ( 3 - 10 ) server configs , e.g. for a startup.

TODO - add links to articles.

I found the following article from codable the lightest and decided to use that as my baseline. I'll share my experiece with the author when I'm done with the setup
https://codeable.io/community/in-pursuit-of-the-perfect-wordpress-server/

Step 1> Setup base server - this is just for testing
Last nite i downloaded Ubuntu Server 14.04.3 and installed it in a fresh VirtialBox VM (2GB ram , 1 Proc). Followed default installation with the following chnages
- for the disk partitioning = use entiner disk WITHOUT LVM
- only select SSH from the server options.
- 
After booting I installed VBoxAdditions and GIT.

Remember  - this server i just for developing my scripts. for WP development i prefer to use the Bitnami prebuilt VM . However for production I do need to know exactly what is installed, so i need to start from the basics.

2> setup Ansible
After trying the install instructions from the codeable article I was not sure if the python modules were setup correctly.
So i picked up the following steps from the Ansible install guide.
http://docs.ansible.com/ansible/intro_installation.html#installation

$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible

went thur without any errors

