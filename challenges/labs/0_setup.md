Challenge Setup

Provider: AWS

Instancias: 172.31.41.99 -> ip-172-31-41-99.us-west-2.compute.internal -> MariaDB -> CM
			172.31.34.102 -> ip-172-31-34-102.us-west-2.compute.internal
			172.31.44.49 -> ip-172-31-44-49.us-west-2.compute.internal
			172.31.46.76 -> ip-172-31-46-76.us-west-2.compute.internal
			172.31.43.231 -> ip-172-31-43-231.us-west-2.compute.internal
			
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,363
extras/7/x86_64                     CentOS-7 - Extras                       449
updates/7/x86_64                    CentOS-7 - Updates                    2,130
repolist: 11,942

Usuarios

$ groupadd comets
$ useradd haley -u 2900 -g comets

$ groupadd planets
$ useradd saturn -u 2800 -g planets









