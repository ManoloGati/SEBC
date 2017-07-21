Challenge 1: Install a MySQL server

MariaDB [(none)]> SHOW VARIABLES LIKE "%version%";
+-------------------------+---------------------+
| Variable_name           | Value               |
+-------------------------+---------------------+
| innodb_version          | 5.5.49-MariaDB-38.0 |
| protocol_version        | 10                  |
| slave_type_conversions  |                     |
| version                 | 5.5.52-MariaDB      |
| version_comment         | MariaDB Server      |
| version_compile_machine | x86_64              |
| version_compile_os      | Linux               |
+-------------------------+---------------------+
7 rows in set (0.00 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hue                |
| metastore          |
| mysql              |
| nav                |
| navms              |
| oozie              |
| performance_schema |
| rman               |
| sentry             |
+--------------------+
11 rows in set (0.00 sec)


MariaDB [(none)]> SELECT Host FROM mysql.user;
+-----------------+
| Host            |
+-----------------+
| %               |
| %               |
| %               |
| %               |
| %               |
| %               |
| %               |
| %               |
| 127.0.0.1       |
| ::1             |
| ip-172-31-41-99 |
| localhost       |
+-----------------+
12 rows in set (0.00 sec)



