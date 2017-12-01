
# The command and output for hdfs dfs -ls /user #

    [root@ip-172-31-28-107 cloudera-scm-server]# hdfs dfs -ls /user
	Found 9 items
	drwxr-xr-x   - cloudera cloudera            0 2017-12-01 19:31 /user/cloudera
	drwxr-xr-x   - haley    haley               0 2017-12-01 19:32 /user/haley
	drwxr-xr-x   - hdfs     supergroup          0 2017-12-01 19:31 /user/hdfs
	drwxrwxrwx   - mapred   hadoop              0 2017-12-01 19:21 /user/history
	drwxrwxr-t   - hive     hive                0 2017-12-01 19:22 /user/hive
	drwxrwxr-x   - hue      hue                 0 2017-12-01 19:22 /user/hue
	drwxrwxr-x   - oozie    oozie               0 2017-12-01 19:22 /user/oozie
	drwxr-xr-x   - saturn   saturn              0 2017-12-01 19:32 /user/saturn
	drwxr-x--x   - spark    spark               0 2017-12-01 19:21 /user/spark
	[root@ip-172-31-28-107 cloudera-scm-server]#


# The command and output from the CM API call ../api/v14/hosts #

	{
	  "items" : [ {
	    "hostId" : "755432b5-1414-4f3f-a58c-b7ebaaf365ee",
	    "ipAddress" : "172.31.16.231",
	    "hostname" : "ip-172-31-16-231.ec2.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-28-107.ec2.internal:7180/cmf/hostRedirect/755432b5-1414-4f3f-a58c-b7ebaaf365ee",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 33567498240
	  }, {
	    "hostId" : "efc6d304-aa98-4993-a86d-521d7e4536fc",
	    "ipAddress" : "172.31.18.175",
	    "hostname" : "ip-172-31-18-175.ec2.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-28-107.ec2.internal:7180/cmf/hostRedirect/efc6d304-aa98-4993-a86d-521d7e4536fc",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 33567498240
	  }, {
	    "hostId" : "323f7452-07d6-4c9c-8f96-7bd265b8333b",
	    "ipAddress" : "172.31.24.5",
	    "hostname" : "ip-172-31-24-5.ec2.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-28-107.ec2.internal:7180/cmf/hostRedirect/323f7452-07d6-4c9c-8f96-7bd265b8333b",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 33567498240
	  }, {
	    "hostId" : "f1731ac3-fefe-473b-8dbf-ec0cc8ecc146",
	    "ipAddress" : "172.31.28.107",
	    "hostname" : "ip-172-31-28-107.ec2.internal",
	    "rackId" : "/default",
	    "hostUrl" : "http://ip-172-31-28-107.ec2.internal:7180/cmf/hostRedirect/f1731ac3-fefe-473b-8dbf-ec0cc8ecc146",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ],
	    "commissionState" : "COMMISSIONED",
	    "numCores" : 8,
	    "numPhysicalCores" : 4,
	    "totalPhysMemBytes" : 33567498240
	  } ]
	}





# The command and output from the CM API call ../api/v8/clusters/<githubName>/
services #


	{
	  "items" : [ {
	    "name" : "cluster",
	    "displayName" : " soaprofessionals",
	    "version" : "CDH5",
	    "fullVersion" : "5.9.3",
	    "maintenanceMode" : false,
	    "maintenanceOwners" : [ ]
	  } ]
	}