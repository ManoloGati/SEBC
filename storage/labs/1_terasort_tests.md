HDFS Lab: Test HDFS throughput

- creacion de usuario 
$ useradd manologati -d /home/manologati -p manologati -s /bin/bash

- Verificar la carpeta /user con hfds
$ sudo -u hdfs hdfs dfs -ls /
- Verificar que usuarios estan en la carpeta /user 
$  sudo -u hdfs hdfs dfs -ls /user/
- Al no estar el usuario creado se debe crear la carpeta con el nombre del usuario creado
$ sudo -u hdfs hdfs dfs -mkdir /user/manologati
- Verificar la carpeta creada con el nombre de usuario y aqui vemos que pertenece al usuario hdfs
$ sudo -u hdfs hdfs dfs -ls /user/
- Asignar la carpeta al usuario creado
$ sudo -u hdfs hdfs dfs -chown manologati:manologati /user/manologati
- Verificar que haya quedado asignado el usuario a la carpeta
$ sudo -u hdfs hdfs dfs -ls /user/

- Crear un archivo con teragen
$ sudo -u manologati time hadoop jar hadoop-examples.jar teragen -Dmapred.compress.map.output=false -Dmapreduce.jobs.maps=4 32000 /user/manologati/teragen

- ejecutar terasort
$ sudo -u manologati time hadoop jar hadoop-examples.jar terasort /user/manologati/teragen /user/manologati/terasort