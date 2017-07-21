Challenge 1: Install a MySQL server

Configurar swap linux
$ cat /proc/sys/vm/swappiness (te muestra el valor de swap)
$ sudo sysctl -w vm.swappiness=1 (asignar el valor de swap a 1)

chequear disable transparent hugepage
$ cd /sys/kernel/mm/transparent_hugepage/
en el archivo enable debe aparecer 'madviser never'

Instalar MariaDB
$ sudo yum install mariadb-server
$ sudo service mariadb stop

configurar el archivo my.cnf
$ sudo vi my.cnf
insertar el valor transaction-isolation = READ_COMMITTED y otros valores

Iniciar el servicio MariaDB
$ sudo service mariadb start

Configurar usuario mariadb
$ sudo /usr/bin/mysql_secure_installation
pass:123456

Copiar el archivo mysql-connector-java-5.1.42.tar.gz en todas las instancias y ejecutar los siguientes comandos
$ tar zxvf mysql-connector-java-5.1.42.tar.gz
$ sudo mkdir -p /usr/share/java/
$ sudo cp mysql-connector-java-5.1.42/mysql-connector-java-5.1.42-bin.jar /usr/share/java/mysql-connector-java.jar

Creando base de datos
mysql> mysql -u root -p123456

mysql> create database amon DEFAULT CHARACTER SET utf8;
mysql> grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon_password'; -- ACTIVE MONITOR

mysql> create database rman DEFAULT CHARACTER SET utf8;
mysql> grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman_password'; -- REPORT MANAGER

mysql> create database metastore DEFAULT CHARACTER SET utf8;
mysql> grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive_password'; -- HIVE

mysql> create database sentry DEFAULT CHARACTER SET utf8;
mysql> grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'sentry_password'; --

mysql> create database nav DEFAULT CHARACTER SET utf8;
mysql> grant all on nav.* TO 'nav'@'%' IDENTIFIED BY 'nav_password'; --

mysql> create database navms DEFAULT CHARACTER SET utf8;
mysql> grant all on navms.* TO 'navms'@'%' IDENTIFIED BY 'navms_password';

mysql> create database hue DEFAULT CHARACTER SET utf8;
mysql> grant all on hue.* TO 'hue'@'%' IDENTIFIED BY 'hue_password';

mysql> create database oozie DEFAULT CHARACTER SET utf8;
mysql> grant all on oozie.* TO 'oozie'@'%' IDENTIFIED BY 'oozie_password';