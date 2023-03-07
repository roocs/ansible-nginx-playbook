# ansible-nginx-playbook
Ansible playbook to install nginx as data node for CDS


Using official nginx role:
https://github.com/nginxinc/ansible-role-nginx

Role for ssl certs:
https://galaxy.ansible.com/jdauphant/ssl-certs

## Run playbook

Do things as root:
```
sudo -i
```

Install ansible:
```
yum update
yum install epel-release
yum install ansible
alternatives --config python
```

Get the playbook:
```
mkdir /opt/roocs
cd /opt/roocs

git clone https://github.com/cehbrecht/ansible-nginx-playbook.git
cd ansible-nginx-playbook
```

Run ansible:
```
make play
```

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


