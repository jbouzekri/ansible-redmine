# Redmine Playbook

An ansible playbook to install redmine on a Debian production server

## Introduction

This playbook installs the following packages :

## Usage

Install ansible in your host machine : [How to install ansible](http://docs.ansible.com/ansible/intro_installation.html#latest-releases-via-apt-ubuntu).

The remote user needs to be in the sudo group :

```
apt-get install sudo
adduser debian sudo
```

Then create your inventory file and run the playbook :

```
cd /tmp
git clone git://github.com/jbouzekri/ansible-redmine --recursive
cd ansible-redmine
cp hosts.example hosts
# edit hosts file to update the ip to your own (or use a hostname)
ansible-playbook -i hosts site.yml -u debian --ask-sudo-pass --ask-pass
```
