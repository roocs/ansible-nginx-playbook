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
dnf update
dnf install epel-release
dnf install ansible
```

Get the playbook:
```
mkdir /opt/roocs
cd /opt/roocs

git clone https://github.com/roocs/ansible-nginx-playbook.git
cd ansible-nginx-playbook
```

Available settings:
```
less group_vars/all
```

Customize settings:
```
vim custom.yml
```

Example: `etc/dkrz.yml`

Run ansible:
```
make play
```

## Test with vagrant

Spin up AlmaLinux 9.x VM:
```
vagrant up
```

Login to VM
```
vagrant ssh
```

Install ansible:
```
sudo dnf update
sudo dnf install epel-release
sudo dnf install ansible
```

Run ansible:
```
cd /vagrant
make play
```

Check nginx:
http://192.168.128.100/


