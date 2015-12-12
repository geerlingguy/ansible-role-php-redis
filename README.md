# Ansible Role: PhpRedis

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-php-redis.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-php-redis)

Installs PhpRedis support on RedHat/CentOS/Debian/Ubuntu.

## Requirements

This role doesn't *explicitly* require Redis to be installed, but if you don't have the daemon running somewhere (either on the same server, or somewhere else), this role won't be all that helpful. Check out `geerlingguy.redis` for a simple role to install and configure Redis (either on the same server, or separate servers).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_enablerepo: ""

(RedHat/CentOS only) If you have enabled any additional repositories (might I suggest geerlingguy.repo-epel or geerlingguy.repo-remi), those repositories can be listed under this variable (e.g. `remi,epel`). This can be handy, as an example, if you want to install the latest version of PHP from Remi's repository.

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: geerlingguy.php-redis }

## License

MIT / BSD

## Author Information

This role was created in 2015 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
