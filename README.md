# publicwhip_server

## Introduction

This is the configuration management code that provisions a server for the Ukraine version of [They Vote For You](https://theyvoteforyou.org.au/).

### Provisioning

For starting a local VM for testing provisioning you will need [Vagrant](https://www.vagrantup.com/).
For configuration management you will need [Ansible](http://docs.ansible.com/).Also:

    vagrant plugin install vagrant-hostsupdater

Create a file `.vault_password_file.txt` with the secret password used to encrypt the secret info in this repo.

You can easily create a local test server with:

    vagrant up

To provision the production server run:

    ansible-playbook --user=root -i hosts playbook.yml

### Deployment

Deployment is done from the [main repository](https://github.com/OPORA/publicwhip) using Mina. See the readme there for instructions.
