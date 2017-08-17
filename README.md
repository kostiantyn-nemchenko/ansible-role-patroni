# Ansible Role for Patroni

An Ansible role which installs and configures [Patroni](https://github.com/zalando/patroni/) service on Ubuntu servers.

## Requirements

- **root access**

  _This role requires root privileges, so tell ansible to use `become: true` in any [convenient way](http://docs.ansible.com/ansible/latest/become.html) for you._

- **etcd endpoint**

  _This role temporary supports only etcd as distributed configuration store. Integration with other DCSs like Consul or ZooKeeper is on the way._

- **PostgreSQL server**

  _Currently this role relies on already installed postgresql server. An opportunity to initialize new cluster if it does not exist will be added in the near future._

## Role Variables

Coming soon.

## Dependencies

* retr0h.etcd

_Note: It doesn't really matter which ansible role you use for setting up etcd. However, it is assumed that you have already installed etcd cluster and it is up and running._

## Example Playbook

    - hosts: postgresql-servers
      become: yes
      roles:
        - patroni
