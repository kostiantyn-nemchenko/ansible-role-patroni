# Ansible Role for Patroni

An Ansible role which installs and configures [Patroni](https://github.com/zalando/patroni/) service on Ubuntu servers.

## Requirements

- **Ubuntu 16+**

  _As for now, this role works only on Ubuntu 16.04 and above._

- **root access**

  _This role requires root privileges, so tell ansible to use `become: true` in any [convenient way](http://docs.ansible.com/ansible/latest/become.html) for you._

- **etcd or consul endpoint**

  _Temporary there is no support of ZooKeeper as distributed configuration store._

- **PostgreSQL server**

  _Currently this role relies on already installed postgresql server. An opportunity to initialize new cluster if it does not exist will be added in the near future._

## Role Variables

Coming soon.

## Dependencies

* [**retr0h.etcd**](https://github.com/retr0h/ansible-etcd) - If you want to leave etcd as default distributed configuration store
* [**brianshumate.consul**](https://github.com/brianshumate/ansible-consul) - If you prefer to use consul as distributed configuration store

## Example Playbook

    - hosts: postgresql-servers
      become: yes
      roles:
        - patroni
