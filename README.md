# Ansible Role for Patroni

[![Build Status](https://travis-ci.org/kostiantyn-nemchenko/ansible-role-patroni.svg?branch=master)](https://travis-ci.org/kostiantyn-nemchenko/ansible-role-patroni)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kostiantyn--nemchenko.patroni-blue.svg)](https://galaxy.ansible.com/kostiantyn-nemchenko/patroni/)

An Ansible role which installs and configures [Patroni](https://github.com/zalando/patroni/) - HA solution for PostgreSQL.

## Requirements

- **root access**

  _This role requires root privileges, so tell ansible to use `become: true` in any [convenient way](http://docs.ansible.com/ansible/latest/become.html) for you._

## Role Variables

Coming soon.

## Dependencies

  _Depending on your preferences, you can use one of the following Ansible roles to setup etcd, Consul or ZooKeeper cluster:_
* [**retr0h.etcd**](https://github.com/retr0h/ansible-etcd)
* [**brianshumate.consul**](https://github.com/brianshumate/ansible-consul)
* [**AnsibleShipyard.ansible-zookeeper**](https://github.com/AnsibleShipyard/ansible-zookeeper)

## Example Playbook

    - hosts: postgresql-servers
      become: yes
      roles:
        - patroni
