Challenge 5 - Kerberize the cluster

Los cuatro pilares en seguridad son:

1- Autenticacion - soy quien digo ser?
	Tecnologias:
	CM
		- Active Directory, LDAP
	CDH
		- Kerberos (AD-MIT)
	
	
	Opciones:
	A) AD / KDC (La mejor opocion)
	B) AD + MIT KDC
	C) Local

	Nunca colocar los nombres de los host en mayusculas - kerberos no los entiende
	
2- Autorizacion - Puedo hacer eso?
	Tecnologias:
	CM
		- Full admin
		- Operador
		- Usuario read only
	CDH
		- HDFS -POSIX
		- HIVE, IMPALA, SENTRY
		- KAFKA

3- Accountability - Que yo fui!
	CM
		- NAvigator
		
4- Privacidad - Solo yo se!
	CM
		- TLS/SSL
		
		
FRASE: "En un cluster de seguridad solo se usa la interfaz de red asociada al FQDN de cada nodo para todo trafico relacionado a Hadoop! en caso de dudas complementarlo con Cloudera!"