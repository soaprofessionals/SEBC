## yum ##

Comando:
    
	ls /etc/yum.repos.d

Salida:

	[root@ip-172-31-28-107 ec2-user]# ls /etc/yum.repos.d
	cloudera-manager.repo  redhat.repo                     redhat-rhui.repo
	MariaDB.repo           redhat-rhui-client-config.repo  rhui-load-balancers.conf
	[root@ip-172-31-28-107 ec2-user]#

## prepare database ##

    ./scm_prepare_database.sh mysql -h ec2-34-227-58-31.compute-1.amazonaws.com -utemp -ptemp --scm-host ec2-34-226-208-48.compute-1.amazonaws.com scm scm PassEdgar_1

Salida:

	[root@ip-172-31-28-107 schema]# ./scm_prepare_database.sh mysql -h ec2-34-227-58-31.compute-1.amazonaws.com -utemp -ptemp --scm-host ec2-34-226-208-48.compute-1.amazonaws.com --force scm scm PassEdgar_1
	JAVA_HOME=/usr/java/jdk1.8.0_151
	Verifying that we can write to /etc/cloudera-scm-server
	[                          main] DbProvisioner                  ERROR Exception when creating/dropping database with user 'temp' and jdbc url 'jdbc:mysql://ec2-34-227-58-31.compute-1.amazonaws.com/?useUnicode=true&characterEncoding=UTF-8'
	java.sql.SQLException: Can't create database 'scm'; database exists
	        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:964)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3973)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3909)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2527)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2680)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2483)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2441)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.StatementImpl.executeInternal(StatementImpl.java:845)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:745)[mysql-connector-java.jar:5.1.44]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner.java:286)[db-common-5.11.0.jar:]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.java:95)[db-common-5.11.0.jar:]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:110)[db-common-5.11.0.jar:]
	[                          main] DbProvisioner                  ERROR Stack Trace:
	java.sql.SQLException: Can't create database 'scm'; database exists
	        at com.mysql.jdbc.SQLError.createSQLException(SQLError.java:964)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3973)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.checkErrorPacket(MysqlIO.java:3909)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.sendCommand(MysqlIO.java:2527)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.MysqlIO.sqlQueryDirect(MysqlIO.java:2680)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2483)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.ConnectionImpl.execSQL(ConnectionImpl.java:2441)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.StatementImpl.executeInternal(StatementImpl.java:845)[mysql-connector-java.jar:5.1.44]
	        at com.mysql.jdbc.StatementImpl.execute(StatementImpl.java:745)[mysql-connector-java.jar:5.1.44]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.executeSql(DbProvisioner.java:286)[db-common-5.11.0.jar:]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.doMain(DbProvisioner.java:95)[db-common-5.11.0.jar:]
	        at com.cloudera.enterprise.dbutil.DbProvisioner.main(DbProvisioner.java:110)[db-common-5.11.0.jar:]
	--> Error 1, ignoring (because force flag is set)
	Creating SCM configuration file in /etc/cloudera-scm-server
	Executing:  /usr/java/jdk1.8.0_151/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
	[                          main] DbCommandExecutor              INFO  Successfully connected to database.
	All done, your SCM database is configured correctly!





