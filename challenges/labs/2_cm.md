Challenge 2: Install Cloudera Manager 5.11

bajar el repo 5.11.1
$ sudo yum install wget
$ wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
editar el archivo y colocarle la version a bajar 5.11.1
$ sudo mv /home/centos/cloudera-manager.repo /etc/yum.repos.d/

[root@ip-172-31-41-99 centos]# ls /etc/yum.repos.d
CentOS-Base.repo       CentOS-fasttrack.repo  CentOS-Vault.repo
CentOS-CR.repo         CentOS-Media.repo      cloudera-manager.repo
CentOS-Debuginfo.repo  CentOS-Sources.repo

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





