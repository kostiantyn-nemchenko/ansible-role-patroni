# Ansible Role for Patroni

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kostiantyn--nemchenko.patroni-blue.svg)](https://galaxy.ansible.com/kostiantyn-nemchenko/patroni/)

An Ansible role which installs and configures [Patroni](https://github.com/zalando/patroni/) - HA solution for PostgreSQL.

### Help Wanted! If you encountered any difficulties with deploying the role into your environment, noticed a bug or a missing feature or just have an idea of how this project could be enhanced, please feel free to file an issue.

## Requirements

This role requires root privileges, so tell ansible to use `become: true` in any [convenient way](http://docs.ansible.com/ansible/latest/become.html) for you.

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
        - kostiantyn-nemchenko.patroni

## Example Inventory

      [patroni]
      patroni1 ansible_host=192.168.0.1
      patroni2 ansible_host=192.168.0.2
      patroni3 ansible_host=192.168.0.3

      [etcd]
      patroni1 ansible_host=192.168.0.1
      patroni2 ansible_host=192.168.0.2
      patroni3 ansible_host=192.168.0.3

## License

MIT

## Author Information
Kostiantyn Nemchenko <kostiantyn.nemchenko@gmail.com>

