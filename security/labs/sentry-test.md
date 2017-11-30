[root@ip-172-31-30-163 ec2-user]# sudo george
sudo: george: command not found
[root@ip-172-31-30-163 ec2-user]# su george
[george@ip-172-31-30-163 ec2-user]$ clear
[george@ip-172-31-30-163 ec2-user]$ kinit george
Password for george@AMAZONAWS.COM:
[george@ip-172-31-30-163 ec2-user]$ klist-fe
bash: klist-fe: command not found
[george@ip-172-31-30-163 ec2-user]$ klist -fe
Ticket cache: FILE:/tmp/krb5cc_1100
Default principal: george@AMAZONAWS.COM

Valid starting       Expires              Service principal
11/30/2017 00:20:46  12/01/2017 00:20:46  krbtgt/AMAZONAWS.COM@AMAZONAWS.COM
        renew until 12/07/2017 00:20:46, Flags: FRI
        Etype (skey, tkt): arcfour-hmac, arcfour-hmac
[george@ip-172-31-30-163 ec2-user]$ beeline
Beeline version 1.1.0-cdh5.11.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-19-242.ec2.internal:10000/default;principal=hive/ip-172-31-19-242.ec2.internal@AMAZONAWS.COM
scan complete in 2ms
Connecting to jdbc:hive2://ip-172-31-19-242.ec2.internal:10000/default;principal=hive/ip-172-31-19-242.ec2.internal@AMAZONAWS.COM
Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-19-242.ec2.internal> show tables;
INFO  : Compiling command(queryId=hive_20171130002323_783c4deb-7dd5-41a2-822d-9d5b36b6e17e): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171130002323_783c4deb-7dd5-41a2-822d-9d5b36b6e17e); Time taken: 0.07 seconds
INFO  : Executing command(queryId=hive_20171130002323_783c4deb-7dd5-41a2-822d-9d5b36b6e17e): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171130002323_783c4deb-7dd5-41a2-822d-9d5b36b6e17e); Time taken: 0.129 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.284 seconds)
0: jdbc:hive2://ip-172-31-19-242.ec2.internal>



[ferdinand@ip-172-31-30-163 ec2-user]$ kinit
Password for ferdinand@AMAZONAWS.COM:
[ferdinand@ip-172-31-30-163 ec2-user]$ klist -fe
Ticket cache: FILE:/tmp/krb5cc_1200
Default principal: ferdinand@AMAZONAWS.COM

Valid starting       Expires              Service principal
11/30/2017 00:26:26  12/01/2017 00:26:26  krbtgt/AMAZONAWS.COM@AMAZONAWS.COM
        renew until 12/07/2017 00:26:26, Flags: FRI
        Etype (skey, tkt): arcfour-hmac, arcfour-hmac
[ferdinand@ip-172-31-30-163 ec2-user]$ beeline
Beeline version 1.1.0-cdh5.11.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-19-242.ec2.internal:10000/default;principal=hive/ip-172-31-19-242.ec2.internal@AMAZONAWS.COM
scan complete in 1ms
Connecting to jdbc:hive2://ip-172-31-19-242.ec2.internal:10000/default;principal=hive/ip-172-31-19-242.ec2.internal@AMAZONAWS.COM
Connected to: Apache Hive (version 1.1.0-cdh5.11.2)
Driver: Hive JDBC (version 1.1.0-cdh5.11.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-19-242.ec2.internal> show tables;
INFO  : Compiling command(queryId=hive_20171130002727_60e9cb3b-5e08-4f57-9f0e-bdd0ad28f79e): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171130002727_60e9cb3b-5e08-4f57-9f0e-bdd0ad28f79e); Time taken: 0.089 seconds
INFO  : Executing command(queryId=hive_20171130002727_60e9cb3b-5e08-4f57-9f0e-bdd0ad28f79e): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171130002727_60e9cb3b-5e08-4f57-9f0e-bdd0ad28f79e); Time taken: 0.13 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.305 seconds)
0: jdbc:hive2://ip-172-31-19-242.ec2.internal>



