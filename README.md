# Vagrant Ansible Docker

Vagrant with Ansible, Docker, Blackfire, Xdebug

## Dependencies

* Vagrant

---

## Usage

1. Clone repo and add to root of your project
2. Vagrant up (use `--debug` for more verbose output from **vagrant**)
3. Access **web** on `http://192.168.33.99/`
4. Access **mysql** on `192.168.33.99:3306`
5. 4. Access **elasticsearch** on `192.168.33.99:9200`
6. etc...

---

## Customisation


### System wide **apt** packages

Edit `ansible/vars/all.yml` and add to collect on line 4, looks like `packages: [vim, htop, iotop]`

*Or variables, mysql passwords etc*

### What **ansible** installs (eg. nginx or apache)

Edit `ansible/playbook.yml` *comment/uncomment* **roles** collection.


### What **docker** containers are installed

Edit `ansible/roles/docker/tasks/main.yml` and add includes for extra containers.

---

### Blackfire

animated screen shot of how to use (gif)

---

### Step through


---

[Blog post](http://blog.dashboardhub.io/2015/07/10/phansible-vagrant-docker-npm/)
