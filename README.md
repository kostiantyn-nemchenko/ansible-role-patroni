# Ansible Role for Patroni

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-kostiantyn--nemchenko.patroni-blue.svg)](https://galaxy.ansible.com/kostiantyn-nemchenko/patroni/)

An Ansible role which installs and configures [Patroni](https://github.com/zalando/patroni/) - HA solution for PostgreSQL.

### Help Wanted! If you encountered any difficulties with deploying the role into your environment, noticed a bug or a missing feature or just have an idea of how this project could be enhanced, please feel free to file an issue.

## Requirements

This role requires root privileges, so tell ansible to use `become: true` in any [convenient way](http://docs.ansible.com/ansible/latest/become.html) for you.

## Role Variables

Coming soon.

## Dependencies

There are no dependencies for the role, but Patroni itself needs a DCS (Etcd, Consul, ZooKeeper or Exhibitor) to be installed and configured properly and it's your responsibility to make it up and running before using this role.
Currently, it is supposed that a DCS is prepared. Otherwise, you can try one of the roles below (just uncomment respective section [here](https://github.com/kostiantyn-nemchenko/ansible-role-patroni/blob/master/meta/main.yml#L28) and set `patroni_dcs_exists` variable to false):

* [**andrewrothstein.etcd-cluster**](https://github.com/andrewrothstein/ansible-etcd-cluster)
* [**brianshumate.consul**](https://github.com/brianshumate/ansible-consul)
* [**AnsibleShipyard.ansible-zookeeper**](https://github.com/AnsibleShipyard/ansible-zookeeper)

## Example Playbook

    - hosts: postgresql-servers
      become: yes
      roles:
        - kostiantyn-nemchenko.patroni

## License

MIT

## Author Information
Kostiantyn Nemchenko <kostiantyn.nemchenko@gmail.com>

