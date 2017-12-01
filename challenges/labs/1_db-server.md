[root@veroj1 java]# hostname -f
veroj1.southcentralus.cloudapp.azure.com
[root@veroj1 java]# mysql -V
mysql  Ver 14.14 Distrib 5.6.38, for Linux (x86_64) using  EditLine wrapper
[root@veroj1 java]# mysql -u root -p
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 15
Server version: 5.6.38 MySQL Community Server (GPL)

Copyright (c) 2000, 2017, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| cmf                |
| hive               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| ozzie              |
| performance_schema |
| rman               |
| sentry             |
+--------------------+
13 rows in set (0.00 sec)

mysql> 
