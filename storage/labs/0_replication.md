Laboratorio de HDFS

- Configurar HDFS para alta disponibilidad

- Asignar Name Node a otro host, preferiblemente donde este Second Node
- Crear 3 Journal Node en los diferentes hosts

- Para cada Journal Node crear carpetas vacias y asignarlas en el wizard
JN1: $ mkdir journalnode1
     $ chmod 775 journalnode1/
     $ chown hdfs:hdfs journalnode1/
JN2: $ mkdir journalnode2
     $ chmod 775 journalnode2/
     $ chown hdfs:hdfs journalnode2/
JN3: $ mkdir journalnode3
     $ chmod 775 journalnode3/
     $ chown hdfs:hdfs journalnode3/
	 
- Generar backup para hive
$ mysqldump -u root -p123456 metastore > /home/centos/bkmetastore.sql

- Upgrade metastore 
- Reiniciar hive


- Asignar el httpFs a HUE
