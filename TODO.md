Requested Features
------------------

- [ ] Add support of Exhibitor (ZooKeeper) and Kubernetes.
- [ ] Support of post init/bootstrap scripts that will be executed after initializing the cluster.
- [ ] Manage SSL certificates for Patroni REST API.
- [ ] Support of different PostgreSQL replication modes (synchronous/cascading replication).
- [ ] Support of custom replica creation methods via 3rd party tools like Barman, WAL-E, pgBackRest.

Known Issues
------------

- [ ] PostgreSQL service is required to be disabled at boot time while controlled via patroni.
- [ ] No support of Ubuntu < 16.04.
- [ ] Unable to start PostgreSQL after bootstrapping if its configuration files are missing.
- [ ] Check that patroni_system_user has all needed permissions to patroni_postgresql_data_dir, patroni_postgresql_config_dir, patroni_postgresql_bin_dir, patroni_postgresql_pgpass.
