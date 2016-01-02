# Vagrant Ansible Docker

Vagrant with Ansible, Docker, Blackfire, Xdebug

---

## Contains

* PHP
* MySQL
* Blackfire (profiling) - not recommended to use with xdebug
* Apache or Nginx (recommended only 1 can be installed at a time)
* Docker
    * MySQL
    * Elasticsearch
    * Postgres
    * Redis
    * Selenium
* Npm
    * Bower
    * Grunt
    * Express
    * Socket.io
* Ruby
    * Jekyll
* xhprof (profiling)
* Xdebug (debugging code)

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

[Blog post](http://blog.dashboardhub.io/2015/07/10/phansible-vagrant-docker-npm/)
