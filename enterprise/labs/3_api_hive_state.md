# Write curl statements that stop, start, and check the current state of your Hive service. #

----------

## stop hive ##

    curl http://ec2-54-236-18-63.compute-1.amazonaws.com:7180/api/v12/clusters/soaprofessionals/services/hive/commands/stop



## start hive ##

    curl http://ec2-54-236-18-63.compute-1.amazonaws.com:7180/api/v12/clusters/soaprofessionals/services/hive/commands/start

## state hive ##

    http://ec2-54-236-18-63.compute-1.amazonaws.com:7180/api/v12/clusters/soaprofessionals/services/hive/

Salida:

	{
	  "name" : "hive",
	  "type" : "HIVE",
	  "clusterRef" : {
	"clusterName" : "cluster"
	  },
	  "serviceUrl" : "http://ip-172-31-30-163.ec2.internal:7180/cmf/serviceRedirect/hive",
	  "roleInstancesUrl" : "http://ip-172-31-30-163.ec2.internal:7180/cmf/serviceRedirect/hive/instances",
	  "serviceState" : "STARTED",
	  "healthSummary" : "GOOD",
	  "healthChecks" : [ {
	"name" : "HIVE_HIVEMETASTORES_HEALTHY",
	"summary" : "GOOD",
	"suppressed" : false
	  }, {
	"name" : "HIVE_HIVESERVER2S_HEALTHY",
	"summary" : "GOOD",
	"suppressed" : false
	  } ],
	  "configStalenessStatus" : "FRESH",
	  "clientConfigStalenessStatus" : "FRESH",
	  "maintenanceMode" : false,
	  "maintenanceOwners" : [ ],
	  "displayName" : "Hive",
	  "entityStatus" : "GOOD_HEALTH"
	}