# Vagrant Ansible Docker

Vagrant with Ansible, Docker, Blackfire, Xdebug

## Dependencies

* Vagrant

---

## Usage

1. Clone repo and add to root of your project
2. Vagrant up (use ``--debug` for more verbose output from **vagrant**)
3. Access on `http://192.168.33.99/`

---

## Customisation


### System wide **apt** packages

Edit `ansible/vars/all.yml` and add to collect on line 4, looks like `packages: [vim, htop, iotop]`


### What **ansible** installs (eg. nginx or apache)

Edit `ansible/playbook.yml` *comment/uncomment* **roles** collection.


### What **docker** containers are installed

Edit `ansible/roles/docker/tasks/main.yml` and add includes for extra containers.
