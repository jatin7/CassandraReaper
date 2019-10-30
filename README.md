# CassandraReaper
A setup using Virtualbox, Vagrant and Ansible to create a demo system for  Cassandra Reaper - http://cassandra-reaper.io/


Requirements
------------
- Vagrant 
- Ansible 


#1 On Command Prompt type following command 
git clone https://github.com/jatin7/CassandraReaper/
cd CassandraReaper
vagrant up

#2 Open browser on your local machine
http://192.168.43.201:8080/webui/
Login/Password: admin/admin


#3 To SSH into VM
vagrant ssh reaper1
vagrant ssh reaper2


#4
vagrant halt
or 
vagrant destroy
