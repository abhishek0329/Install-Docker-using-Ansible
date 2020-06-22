Automatic provision of Docker using ansible-playbook
====================================================

Docker-Installation role is bundled with all packages and dependencies required to install docker on host machine. This ansible role will deploy below tools:

	1.Docker ce
	2.Dockered.io
	3.Docker-compose


Requirements
------------

Ansible needs to be installed on master node.

This role is designed for centos 7 and will also work on redhat linux servers.

Role Variables
--------------
There are three varriables defined in this role. They are present in vars/main.yml as mentioned below.

ver: 18.09.6 # Enter the docker version you wish to install. Here I have taken 18.09.6 version as an example.
rel_version: 1.26.0 # Enter the docker-compose release version you wish to install. Here I have taken 1.26.0 version as an example.
os_version: docker-compose-Linux-x86_64 # Enter the docker-compose package depending upon your os.

ref : https://github.com/docker/compose/releases/

Dependencies
------------

There are no dependencies to use this role.

Example Playbook
----------------

This role is simple to use. All you need is to mention the role in your ansible playbook file.

    - hosts: <servers/group>
      become: yes
      become_uesr: root
      roles:
         - Docker-Installation

License
-------

BSD

Author Information
------------------

This role is written by below team members. 

  Name              Contact
Abhishek         email : abhishek.k21@infosys.com
Divyaree         email : divyasree.h@infosys.com
Jaise            email : jaise.augustine@infosys.com
