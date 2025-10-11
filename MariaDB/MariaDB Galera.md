# MariaDB Galera Overview

<br>

# Setting Up MariabDB Galera

```Bash
sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf
```
```Text
[mysqld]
binlog_format=ROW
default-storage-engine=innodb
innodb_autoinc_lock_mode=2
bind-address=0.0.0.0
# Galera Provider Configuration
wsrep_on=ON
wsrep_provider=/usr/lib/galera/libgalera_smm.so
# Galera Cluster Configuration
wsrep_cluster_name="galera_cluster"
wsrep_cluster_address="gcomm://node_1-ip-address,node_2-ip-address,node_3-ip-address"
# Galera Synchronization Configuration
wsrep_sst_method=rsync
# Galera Node Configuration
wsrep_node_address="node_1-ip-address"
wsrep_node_name="node_1"
```
```Bash
sudo systemctl stop mariadb

sudo galera_new_cluster

sudo mariadb
SHOW STATUS LIKE 'wsrep_%';

sudo systemctl start mariadb
```
