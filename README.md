# ansible-nginx-playbook
Ansible playbook to install nginx as data node for CDS


Using official nginx role:
https://github.com/nginxinc/ansible-role-nginx

Role for ssl certs:
https://galaxy.ansible.com/jdauphant/ssl-certs

## Test with vagrant

Spin up AlmaLinux 8.x VM:
```
vagrant up
```

Login to VM
```
vagrant ssh
```

Install ansible:
```
sudo yum update
sudo yum install epel-release
sudo yum install ansible
```

Run ansible:
```
cd /vagrant
make play
```

Check nginx:
http://192.168.128.100/


