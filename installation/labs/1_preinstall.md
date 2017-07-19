Instalacion Cloudera

1. Instalacion de Base de Datos MariaDB

- Configuracion swap
$ cat /proc/sys/vm/swappiness (te muestra el valor de swap)
$ sudo sysctl -w vm.swappiness=1 (asignar el valor de swap a 1)

- Instalar MariaDB
$ sudo yum install mariadb-server
$ sudo service mariadb stop

- Configurar el archivo my.cnf
$ sudo vi my.cnf
insertar el valor transaction-isolation = READ_COMMITTED y otros valores de la guia

- Iniciar servidor
$ sudo service mariadb start

- Configurar usuario MariaDB
$ sudo /usr/bin/mysql_secure_installation
pass:123456

2. Creando bases de datos utilizados por los servicios en Cloudera Manager
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

3. Instalar JDBC driver
- descargar mysql-connector-java-5.1.42.tar.gz, este archivo lo pase de mi maquina local al host a traves de WinSCP
$ tar zxvf mysql-connector-java-5.1.42.tar.gz -- Descomprimir
$ sudo mkdir -p /usr/share/java/ -- crear carpeta 
$ sudo cp mysql-connector-java-5.1.42/mysql-connector-java-5.1.42-bin.jar /usr/share/java/mysql-connector-java.jar -- copiarlo 

4. Instalar Cloudera Manager Server
- bajar el repo de cloudera manager a descargar
$ wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
$ vi cloudera-manager.repo -- editar el archivo y colocarle la version a bajar para este caso 5.11.1
$ sudo mv /home/centos/cloudera-manager.repo /etc/yum.repos.d/ -- mover el archivo modificado

Instalando Cloudera Manager 

-Instal JDK
$ sudo yum install oracle-j2sdk1.7

-Instal daemons, server
$ sudo yum install cloudera-manager-daemons cloudera-manager-server

-Start clouder manager server host
$ sudo service cloudera-scm-server start

5. Preparar BD scm con el sh
$ sudo service cloudera-scm-server stop
$ /usr/share/cmf/schema/scm_prepare_database.sh mysql scm scm 123456 -u root -p123456

6. Iniciar Cloudera MANAGER
$ sudo service cloudera-scm-server start

7. Inspeccionar logs de Cloudera server
