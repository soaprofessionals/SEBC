El comando fue: 

    http://ec2-54-236-18-63.compute-1.amazonaws.com:7180/api/v16/cm/deployment
    

El resultado:

----------


				{
			  "timestamp" : "2017-11-30T17:53:54.167Z",
			  "clusters" : [ {
			    "name" : "cluster",
			    "displayName" : "soaprofessionals",
			    "version" : "CDH5",
			    "fullVersion" : "5.11.2",
			    "services" : [ {
			      "name" : "hive",
			      "type" : "HIVE",
			      "config" : {
			        "items" : [ {
			          "name" : "hive_metastore_database_host",
			          "value" : "ec2-54-236-18-63.compute-1.amazonaws.com",
			          "sensitive" : false
			        }, {
			          "name" : "hive_metastore_database_password",
			          "value" : "PassEdgar_1",
			          "sensitive" : true
			        }, {
			          "name" : "mapreduce_yarn_service",
			          "value" : "yarn",
			          "sensitive" : false
			        }, {
			          "name" : "sentry_service",
			          "value" : "sentry",
			          "sensitive" : false
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "hive-GATEWAY-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "GATEWAY",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-GATEWAY-BASE"
			        }
			      }, {
			        "name" : "hive-GATEWAY-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "GATEWAY",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-GATEWAY-BASE"
			        }
			      }, {
			        "name" : "hive-GATEWAY-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "GATEWAY",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-GATEWAY-BASE"
			        }
			      }, {
			        "name" : "hive-GATEWAY-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "GATEWAY",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-GATEWAY-BASE"
			        }
			      }, {
			        "name" : "hive-HIVEMETASTORE-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "HIVEMETASTORE",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "5w14y2xi5nllakpce9xsldy4v",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
			        }
			      }, {
			        "name" : "hive-HIVESERVER2-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "HIVESERVER2",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "4nock4wfvfhyjdlpqfk5bdy65",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
			        }
			      } ],
			      "displayName" : "Hive",
			      "roleConfigGroups" : [ {
			        "name" : "hive-GATEWAY-BASE",
			        "displayName" : "Gateway Default Group",
			        "roleType" : "GATEWAY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hive"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hive-HIVEMETASTORE-BASE",
			        "displayName" : "Hive Metastore Server Default Group",
			        "roleType" : "HIVEMETASTORE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hive"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "hive_metastore_java_heapsize",
			            "value" : "3769630720",
			            "sensitive" : false
			          }, {
			            "name" : "hive_metastore_server_max_message_size",
			            "value" : "376963072",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hive-HIVESERVER2-BASE",
			        "displayName" : "HiveServer2 Default Group",
			        "roleType" : "HIVESERVER2",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hive"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "hiveserver2_enable_impersonation",
			            "value" : "false",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_java_heapsize",
			            "value" : "3769630720",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_spark_driver_memory",
			            "value" : "966367641",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_spark_executor_cores",
			            "value" : "4",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_spark_executor_memory",
			            "value" : "4732302131",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
			            "value" : "102",
			            "sensitive" : false
			          }, {
			            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
			            "value" : "796",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hive-WEBHCAT-BASE",
			        "displayName" : "WebHCat Server Default Group",
			        "roleType" : "WEBHCAT",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hive"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      } ],
			      "replicationSchedules" : [ ]
			    }, {
			      "name" : "zookeeper",
			      "type" : "ZOOKEEPER",
			      "config" : {
			        "items" : [ {
			          "name" : "enableSecurity",
			          "value" : "true",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "zookeeper-SERVER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "SERVER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "2o32h6zuhhba1y3b1ppkzwmoh",
			            "sensitive" : true
			          }, {
			            "name" : "serverId",
			            "value" : "1",
			            "sensitive" : false
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
			        }
			      }, {
			        "name" : "zookeeper-SERVER-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "SERVER",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "33bmdizff5xumhh7tl8fipnk4",
			            "sensitive" : true
			          }, {
			            "name" : "serverId",
			            "value" : "3",
			            "sensitive" : false
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
			        }
			      }, {
			        "name" : "zookeeper-SERVER-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "SERVER",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "1rjbr3n11lvfgqnq3qpg8esop",
			            "sensitive" : true
			          }, {
			            "name" : "serverId",
			            "value" : "2",
			            "sensitive" : false
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
			        }
			      } ],
			      "displayName" : "ZooKeeper",
			      "roleConfigGroups" : [ {
			        "name" : "zookeeper-SERVER-BASE",
			        "displayName" : "Server Default Group",
			        "roleType" : "SERVER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "zookeeper"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      } ]
			    }, {
			      "name" : "hue",
			      "type" : "HUE",
			      "config" : {
			        "items" : [ {
			          "name" : "database_host",
			          "value" : "ec2-54-236-18-63.compute-1.amazonaws.com",
			          "sensitive" : false
			        }, {
			          "name" : "database_password",
			          "value" : "PassEdgar_1",
			          "sensitive" : true
			        }, {
			          "name" : "database_type",
			          "value" : "mysql",
			          "sensitive" : false
			        }, {
			          "name" : "hive_service",
			          "value" : "hive",
			          "sensitive" : false
			        }, {
			          "name" : "hue_webhdfs",
			          "value" : "hdfs-HTTPFS-62797e3c0c90ffb3d2e04116a6276fa8",
			          "sensitive" : false
			        }, {
			          "name" : "oozie_service",
			          "value" : "oozie",
			          "sensitive" : false
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "hue-HUE_SERVER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "HUE_SERVER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "92yi5gaqov9wvksgm4uto5gv5",
			            "sensitive" : true
			          }, {
			            "name" : "secret_key",
			            "value" : "nqQ3QlPTMtdSIRf9aQzK37BJZg5zpH",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
			        }
			      }, {
			        "name" : "hue-KT_RENEWER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "KT_RENEWER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "41jth9qs38g1s2bgj75tkgl53",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hue-KT_RENEWER-BASE"
			        }
			      } ],
			      "displayName" : "Hue",
			      "roleConfigGroups" : [ {
			        "name" : "hue-HUE_LOAD_BALANCER-BASE",
			        "displayName" : "Load Balancer Default Group",
			        "roleType" : "HUE_LOAD_BALANCER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hue"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hue-HUE_SERVER-BASE",
			        "displayName" : "Hue Server Default Group",
			        "roleType" : "HUE_SERVER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hue"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "hue_server_bind_wildcard",
			            "value" : "true",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hue-KT_RENEWER-BASE",
			        "displayName" : "Kerberos Ticket Renewer Default Group",
			        "roleType" : "KT_RENEWER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hue"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      } ]
			    }, {
			      "name" : "oozie",
			      "type" : "OOZIE",
			      "config" : {
			        "items" : [ {
			          "name" : "hive_service",
			          "value" : "hive",
			          "sensitive" : false
			        }, {
			          "name" : "mapreduce_yarn_service",
			          "value" : "yarn",
			          "sensitive" : false
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "oozie-OOZIE_SERVER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "OOZIE_SERVER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "af2o9uegufcuqce2n9wzlz6wt",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
			        }
			      } ],
			      "displayName" : "Oozie",
			      "roleConfigGroups" : [ {
			        "name" : "oozie-OOZIE_SERVER-BASE",
			        "displayName" : "Oozie Server Default Group",
			        "roleType" : "OOZIE_SERVER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "oozie"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "oozie_database_host",
			            "value" : "ec2-54-236-18-63.compute-1.amazonaws.com",
			            "sensitive" : false
			          }, {
			            "name" : "oozie_database_password",
			            "value" : "PassEdgar_1",
			            "sensitive" : true
			          }, {
			            "name" : "oozie_database_type",
			            "value" : "mysql",
			            "sensitive" : false
			          }, {
			            "name" : "oozie_database_user",
			            "value" : "oozie",
			            "sensitive" : false
			          } ]
			        }
			      } ]
			    }, {
			      "name" : "yarn",
			      "type" : "YARN",
			      "config" : {
			        "items" : [ {
			          "name" : "hdfs_service",
			          "value" : "hdfs",
			          "sensitive" : false
			        }, {
			          "name" : "rm_dirty",
			          "value" : "false",
			          "sensitive" : false
			        }, {
			          "name" : "rm_last_allocation_percentage",
			          "value" : "80",
			          "sensitive" : false
			        }, {
			          "name" : "yarn_service_cgroups",
			          "value" : "false",
			          "sensitive" : false
			        }, {
			          "name" : "yarn_service_lce_always",
			          "value" : "false",
			          "sensitive" : false
			        }, {
			          "name" : "zk_authorization_secret_key",
			          "value" : "RvekmtBuCmBpyNnKa0by4HnFd7SN5O",
			          "sensitive" : true
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "yarn-JOBHISTORY-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "JOBHISTORY",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "5yjvt2uy41j4egvy7jfmbcxhm",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
			        }
			      }, {
			        "name" : "yarn-NODEMANAGER-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "NODEMANAGER",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "3pmb8lienf4deo94lvzu3nqpp",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
			        }
			      }, {
			        "name" : "yarn-NODEMANAGER-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "NODEMANAGER",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "8j0e5cr6as7x7l07s9bottfpy",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
			        }
			      }, {
			        "name" : "yarn-NODEMANAGER-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "NODEMANAGER",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "4b04n1v532ck0e8z7lvhx63e5",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
			        }
			      }, {
			        "name" : "yarn-RESOURCEMANAGER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "RESOURCEMANAGER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "rm_id",
			            "value" : "132",
			            "sensitive" : false
			          }, {
			            "name" : "role_jceks_password",
			            "value" : "3257q2tc4wb402phco5q2fh8o",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
			        }
			      } ],
			      "displayName" : "YARN (MR2 Included)",
			      "roleConfigGroups" : [ {
			        "name" : "yarn-GATEWAY-BASE",
			        "displayName" : "Gateway Default Group",
			        "roleType" : "GATEWAY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "yarn"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "mapred_reduce_tasks",
			            "value" : "12",
			            "sensitive" : false
			          }, {
			            "name" : "mapred_submit_replication",
			            "value" : "1",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "yarn-JOBHISTORY-BASE",
			        "displayName" : "JobHistory Server Default Group",
			        "roleType" : "JOBHISTORY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "yarn"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "yarn-NODEMANAGER-1",
			        "displayName" : "NodeManager Group 1",
			        "roleType" : "NODEMANAGER",
			        "base" : false,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "yarn"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "yarn_nodemanager_heartbeat_interval_ms",
			            "value" : "100",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_local_dirs",
			            "value" : "/yarn/nm",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_log_dirs",
			            "value" : "/yarn/container-logs",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_resource_memory_mb",
			            "value" : "9951",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "yarn-NODEMANAGER-BASE",
			        "displayName" : "NodeManager Default Group",
			        "roleType" : "NODEMANAGER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "yarn"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "rm_cpu_shares",
			            "value" : "1600",
			            "sensitive" : false
			          }, {
			            "name" : "rm_io_weight",
			            "value" : "800",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_heartbeat_interval_ms",
			            "value" : "100",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_local_dirs",
			            "value" : "/yarn/nm",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_log_dirs",
			            "value" : "/yarn/container-logs",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_resource_cpu_vcores",
			            "value" : "6",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_nodemanager_resource_memory_mb",
			            "value" : "13178",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "yarn-RESOURCEMANAGER-BASE",
			        "displayName" : "ResourceManager Default Group",
			        "roleType" : "RESOURCEMANAGER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "yarn"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "yarn_scheduler_maximum_allocation_mb",
			            "value" : "18184",
			            "sensitive" : false
			          }, {
			            "name" : "yarn_scheduler_maximum_allocation_vcores",
			            "value" : "6",
			            "sensitive" : false
			          } ]
			        }
			      } ]
			    }, {
			      "name" : "hdfs",
			      "type" : "HDFS",
			      "config" : {
			        "items" : [ {
			          "name" : "dfs_encrypt_data_transfer_algorithm",
			          "value" : "AES/CTR/NoPadding",
			          "sensitive" : false
			        }, {
			          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
			          "value" : "TTob2DvMp5JoYBVNFyqyz26cnI81at",
			          "sensitive" : true
			        }, {
			          "name" : "fc_authorization_secret_key",
			          "value" : "i2PxdOlRY0cIgJHkKggehAluZJRUUs",
			          "sensitive" : true
			        }, {
			          "name" : "hadoop_security_authentication",
			          "value" : "kerberos",
			          "sensitive" : false
			        }, {
			          "name" : "hadoop_security_authorization",
			          "value" : "true",
			          "sensitive" : false
			        }, {
			          "name" : "http_auth_signature_secret",
			          "value" : "kKjMYBUZ2CPH6uqT8hKBxH6MRG83qu",
			          "sensitive" : true
			        }, {
			          "name" : "rm_dirty",
			          "value" : "false",
			          "sensitive" : false
			        }, {
			          "name" : "rm_last_allocation_percentage",
			          "value" : "20",
			          "sensitive" : false
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "hdfs-BALANCER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "BALANCER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
			        }
			      }, {
			        "name" : "hdfs-DATANODE-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "DATANODE",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "6ftj0y7a6wubpotfgznjzrrc4",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-DATANODE-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "DATANODE",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "5xet67i4l53p8vpbok8ahfu2d",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-DATANODE-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "DATANODE",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "a5j7bp3hpzu73v5sddn1m8hdh",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-FAILOVERCONTROLLER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "FAILOVERCONTROLLER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "2e30eznsib86henombxh4i14u",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
			        }
			      }, {
			        "name" : "hdfs-FAILOVERCONTROLLER-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "FAILOVERCONTROLLER",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "8n9woq8ywwqd26aeltivo7z3m",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
			        }
			      }, {
			        "name" : "hdfs-HTTPFS-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "HTTPFS",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "beojyr93evayfqhl4uptmg41",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
			        }
			      }, {
			        "name" : "hdfs-JOURNALNODE-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "JOURNALNODE",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "1n9mj21m3nsy0v3rnnhrjwbmb",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-JOURNALNODE-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "JOURNALNODE",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "8prvv63dbyo3r95xz8rml7ukl",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-JOURNALNODE-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "JOURNALNODE",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "9tl2asugu763jhlsukhrw9xn1",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-NAMENODE-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "NAMENODE",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "autofailover_enabled",
			            "value" : "true",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_federation_namenode_nameservice",
			            "value" : "nameservice1",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_namenode_quorum_journal_name",
			            "value" : "nameservice1",
			            "sensitive" : false
			          }, {
			            "name" : "namenode_id",
			            "value" : "134",
			            "sensitive" : false
			          }, {
			            "name" : "role_jceks_password",
			            "value" : "5bnqafzj95ul6n1a4ax95mlqd",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
			        }
			      }, {
			        "name" : "hdfs-NAMENODE-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "NAMENODE",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "autofailover_enabled",
			            "value" : "true",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_federation_namenode_nameservice",
			            "value" : "nameservice1",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_namenode_quorum_journal_name",
			            "value" : "nameservice1",
			            "sensitive" : false
			          }, {
			            "name" : "namenode_id",
			            "value" : "141",
			            "sensitive" : false
			          }, {
			            "name" : "role_jceks_password",
			            "value" : "d4dhewgq32c0vttgpbf998iqw",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
			        }
			      } ],
			      "displayName" : "HDFS",
			      "roleConfigGroups" : [ {
			        "name" : "hdfs-BALANCER-BASE",
			        "displayName" : "Balancer Default Group",
			        "roleType" : "BALANCER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hdfs-DATANODE-BASE",
			        "displayName" : "DataNode Default Group",
			        "roleType" : "DATANODE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "datanode_java_heapsize",
			            "value" : "1073741824",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_data_dir_list",
			            "value" : "/dfs/dn",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_datanode_data_dir_perm",
			            "value" : "700",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_datanode_du_reserved",
			            "value" : "5367448780",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_datanode_http_port",
			            "value" : "1006",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_datanode_max_locked_memory",
			            "value" : "4296015872",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_datanode_port",
			            "value" : "1004",
			            "sensitive" : false
			          }, {
			            "name" : "rm_cpu_shares",
			            "value" : "400",
			            "sensitive" : false
			          }, {
			            "name" : "rm_io_weight",
			            "value" : "200",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
			        "displayName" : "Failover Controller Default Group",
			        "roleType" : "FAILOVERCONTROLLER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hdfs-GATEWAY-BASE",
			        "displayName" : "Gateway Default Group",
			        "roleType" : "GATEWAY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "dfs_client_use_trash",
			            "value" : "true",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hdfs-HTTPFS-BASE",
			        "displayName" : "HttpFS Default Group",
			        "roleType" : "HTTPFS",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hdfs-JOURNALNODE-BASE",
			        "displayName" : "JournalNode Default Group",
			        "roleType" : "JOURNALNODE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "dfs_journalnode_edits_dir",
			            "value" : "/dfs/jn",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hdfs-NAMENODE-BASE",
			        "displayName" : "NameNode Default Group",
			        "roleType" : "NAMENODE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "dfs_name_dir_list",
			            "value" : "/dfs/nn",
			            "sensitive" : false
			          }, {
			            "name" : "dfs_namenode_servicerpc_address",
			            "value" : "8022",
			            "sensitive" : false
			          }, {
			            "name" : "namenode_java_heapsize",
			            "value" : "3769630720",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "hdfs-NFSGATEWAY-BASE",
			        "displayName" : "NFS Gateway Default Group",
			        "roleType" : "NFSGATEWAY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "hdfs-SECONDARYNAMENODE-BASE",
			        "displayName" : "SecondaryNameNode Default Group",
			        "roleType" : "SECONDARYNAMENODE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "hdfs"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "fs_checkpoint_dir_list",
			            "value" : "/dfs/snn",
			            "sensitive" : false
			          }, {
			            "name" : "secondary_namenode_java_heapsize",
			            "value" : "3769630720",
			            "sensitive" : false
			          } ]
			        }
			      } ],
			      "replicationSchedules" : [ ],
			      "snapshotPolicies" : [ ]
			    }, {
			      "name" : "impala",
			      "type" : "IMPALA",
			      "config" : {
			        "items" : [ {
			          "name" : "hdfs_service",
			          "value" : "hdfs",
			          "sensitive" : false
			        }, {
			          "name" : "hive_service",
			          "value" : "hive",
			          "sensitive" : false
			        }, {
			          "name" : "llama_am_ha_zk_auth_secret_key",
			          "value" : "HxHRxtVCqowQVmuT73lDp4W3zfoLTR",
			          "sensitive" : true
			        }, {
			          "name" : "rm_dirty",
			          "value" : "true",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "impala-CATALOGSERVER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "CATALOGSERVER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "9a6h9kn3o95u72irlomg8cqe3",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "impala-CATALOGSERVER-BASE"
			        }
			      }, {
			        "name" : "impala-IMPALAD-3c4eaf082c4823afca5697fd6138c9e5",
			        "type" : "IMPALAD",
			        "hostRef" : {
			          "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "230ik0lgoxetxjcbu496361rp",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "impala-IMPALAD-BASE"
			        }
			      }, {
			        "name" : "impala-IMPALAD-62797e3c0c90ffb3d2e04116a6276fa8",
			        "type" : "IMPALAD",
			        "hostRef" : {
			          "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "bxcmqzq85ohf1z7cflg61dnh5",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "impala-IMPALAD-1"
			        }
			      }, {
			        "name" : "impala-IMPALAD-722dc38ba432d2571cde0495f3b59d05",
			        "type" : "IMPALAD",
			        "hostRef" : {
			          "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "42y2y64xmdnv2b1flqs41mxx0",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "impala-IMPALAD-BASE"
			        }
			      }, {
			        "name" : "impala-STATESTORE-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "STATESTORE",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "cgxvc1wmc8hd7jec2vnena0ai",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "impala-STATESTORE-BASE"
			        }
			      } ],
			      "displayName" : "Impala",
			      "roleConfigGroups" : [ {
			        "name" : "impala-CATALOGSERVER-BASE",
			        "displayName" : "Impala Catalog Server Default Group",
			        "roleType" : "CATALOGSERVER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "impala"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "catalogd_embedded_jvm_heapsize",
			            "value" : "3124756480",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "impala-IMPALAD-1",
			        "displayName" : "Impala Daemon Group 1",
			        "roleType" : "IMPALAD",
			        "base" : false,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "impala"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "impalad_memory_limit",
			            "value" : "3504340992",
			            "sensitive" : false
			          }, {
			            "name" : "scratch_dirs",
			            "value" : "/impala/impalad",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "impala-IMPALAD-BASE",
			        "displayName" : "Impala Daemon Default Group",
			        "roleType" : "IMPALAD",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "impala"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "impalad_memory_limit",
			            "value" : "268435456",
			            "sensitive" : false
			          }, {
			            "name" : "scratch_dirs",
			            "value" : "/impala/impalad",
			            "sensitive" : false
			          } ]
			        }
			      }, {
			        "name" : "impala-LLAMA-BASE",
			        "displayName" : "Impala Llama ApplicationMaster Default Group",
			        "roleType" : "LLAMA",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "impala"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "impala-STATESTORE-BASE",
			        "displayName" : "Impala StateStore Default Group",
			        "roleType" : "STATESTORE",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "impala"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      } ]
			    }, {
			      "name" : "sentry",
			      "type" : "SENTRY",
			      "config" : {
			        "items" : [ {
			          "name" : "hdfs_service",
			          "value" : "hdfs",
			          "sensitive" : false
			        }, {
			          "name" : "sentry_server_database_host",
			          "value" : "ip-172-31-30-163.ec2.internal",
			          "sensitive" : false
			        }, {
			          "name" : "sentry_server_database_password",
			          "value" : "PassEdgar_1",
			          "sensitive" : true
			        }, {
			          "name" : "sentry_service_admin_group",
			          "value" : "hive,impala,hue,solr,kafka,edgar",
			          "sensitive" : false
			        }, {
			          "name" : "zookeeper_service",
			          "value" : "zookeeper",
			          "sensitive" : false
			        } ]
			      },
			      "roles" : [ {
			        "name" : "sentry-SENTRY_SERVER-304cb1bfacc7079f7b38a0aa1cdaecd5",
			        "type" : "SENTRY_SERVER",
			        "hostRef" : {
			          "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "role_jceks_password",
			            "value" : "atgty9rrq65wwvi3boi0sma0n",
			            "sensitive" : true
			          } ]
			        },
			        "roleConfigGroupRef" : {
			          "roleConfigGroupName" : "sentry-SENTRY_SERVER-BASE"
			        }
			      } ],
			      "displayName" : "Sentry",
			      "roleConfigGroups" : [ {
			        "name" : "sentry-GATEWAY-BASE",
			        "displayName" : "Gateway Default Group",
			        "roleType" : "GATEWAY",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "sentry"
			        },
			        "config" : {
			          "items" : [ ]
			        }
			      }, {
			        "name" : "sentry-SENTRY_SERVER-BASE",
			        "displayName" : "Sentry Server Default Group",
			        "roleType" : "SENTRY_SERVER",
			        "base" : true,
			        "serviceRef" : {
			          "clusterName" : "cluster",
			          "serviceName" : "sentry"
			        },
			        "config" : {
			          "items" : [ {
			            "name" : "sentry_server_java_heapsize",
			            "value" : "268435456",
			            "sensitive" : false
			          } ]
			        }
			      } ]
			    } ],
			    "parcels" : [ {
			      "product" : "CDH",
			      "version" : "5.11.2-1.cdh5.11.2.p0.4",
			      "stage" : "DISTRIBUTED",
			      "clusterRef" : {
			        "clusterName" : "cluster"
			      }
			    }, {
			      "product" : "CDH",
			      "version" : "5.11.2-1.cdh5.11.2.p0.4",
			      "stage" : "ACTIVATED",
			      "clusterRef" : {
			        "clusterName" : "cluster"
			      }
			    } ],
			    "uuid" : "c00ea01f-a5f9-4ae4-b479-1ae1507a024c"
			  } ],
			  "hosts" : [ {
			    "hostId" : "72ab3feb-5f55-4e5d-b534-24cbf84c1372",
			    "ipAddress" : "172.31.19.242",
			    "hostname" : "ip-172-31-19-242.ec2.internal",
			    "rackId" : "/default",
			    "config" : {
			      "items" : [ ]
			    }
			  }, {
			    "hostId" : "8e48ce77-6ae0-4715-b20a-f75140c5cfd4",
			    "ipAddress" : "172.31.19.253",
			    "hostname" : "ip-172-31-19-253.ec2.internal",
			    "rackId" : "/default",
			    "config" : {
			      "items" : [ ]
			    }
			  }, {
			    "hostId" : "d990e0cc-adf3-4fe6-8ced-8279423ef2b5",
			    "ipAddress" : "172.31.25.222",
			    "hostname" : "ip-172-31-25-222.ec2.internal",
			    "rackId" : "/default",
			    "config" : {
			      "items" : [ ]
			    }
			  }, {
			    "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565",
			    "ipAddress" : "172.31.30.163",
			    "hostname" : "ip-172-31-30-163.ec2.internal",
			    "rackId" : "/default",
			    "config" : {
			      "items" : [ ]
			    }
			  } ],
			  "users" : [ {
			    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-722dc38ba432d2571cde0495f3b59d05",
			    "roles" : [ "ROLE_USER" ],
			    "pwHash" : "45f08639c1fc8c1c79dd2b68d9f9d3bbd1c5a0bb70000afab0e580c93810dcfc",
			    "pwSalt" : 1830773075995572987,
			    "pwLogin" : true
			  }, {
			    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-722dc38ba432d2571cde0495f3b59d05",
			    "roles" : [ "ROLE_USER" ],
			    "pwHash" : "6161b22dd8275b53fbfbecca92d068e9ec2eceadd1cdf36f8304d4c3e2e7dd6f",
			    "pwSalt" : -3506879530172299365,
			    "pwLogin" : true
			  }, {
			    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-722dc38ba432d2571cde0495f3b59d05",
			    "roles" : [ "ROLE_USER" ],
			    "pwHash" : "f7c159c86981a15a986ebeaa48492c2a2da4a6867adccf33e28474750a9f2f23",
			    "pwSalt" : -3479649159313918210,
			    "pwLogin" : true
			  }, {
			    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-722dc38ba432d2571cde0495f3b59d05",
			    "roles" : [ "ROLE_USER" ],
			    "pwHash" : "91448deed825ccf9d97192f260928ef5d8d66d5821fcc3606210d83a2158e2b6",
			    "pwSalt" : -5405805018916454454,
			    "pwLogin" : true
			  }, {
			    "name" : "admin",
			    "roles" : [ "ROLE_LIMITED" ],
			    "pwHash" : "02dab7388775c78daa0294e32742fe425bee733c40c705b4f414f033340292b2",
			    "pwSalt" : -5881417153161845994,
			    "pwLogin" : true
			  }, {
			    "name" : "minotaur",
			    "roles" : [ "ROLE_CONFIGURATOR" ],
			    "pwHash" : "de4691506ce1507a27409b38f64ed741d50631308cc3c60436d84bbfb4dce627",
			    "pwSalt" : 8994715392387380885,
			    "pwLogin" : true
			  }, {
			    "name" : "soaprofessionals",
			    "roles" : [ "ROLE_ADMIN" ],
			    "pwHash" : "e045a27de7811acbea6c45f24db157c750c0e04c49ce0fa1dbba4d79160e760a",
			    "pwSalt" : -3549010338409941591,
			    "pwLogin" : true
			  } ],
			  "versionInfo" : {
			    "version" : "5.11.0",
			    "buildUser" : "jenkins",
			    "buildTimestamp" : "20170412-1255",
			    "gitHash" : "70cb1442626406432a6e7af5bdf206a384ca3f98",
			    "snapshot" : false
			  },
			  "managementService" : {
			    "name" : "mgmt",
			    "type" : "MGMT",
			    "config" : {
			      "items" : [ ]
			    },
			    "roles" : [ {
			      "name" : "mgmt-ALERTPUBLISHER-722dc38ba432d2571cde0495f3b59d05",
			      "type" : "ALERTPUBLISHER",
			      "hostRef" : {
			        "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "role_jceks_password",
			          "value" : "7omgxhdt11igysv2eb7z63ejx",
			          "sensitive" : true
			        } ]
			      },
			      "roleConfigGroupRef" : {
			        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
			      }
			    }, {
			      "name" : "mgmt-EVENTSERVER-722dc38ba432d2571cde0495f3b59d05",
			      "type" : "EVENTSERVER",
			      "hostRef" : {
			        "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "role_jceks_password",
			          "value" : "5jv2x7soxwm6kmk73ger123ae",
			          "sensitive" : true
			        } ]
			      },
			      "roleConfigGroupRef" : {
			        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
			      }
			    }, {
			      "name" : "mgmt-HOSTMONITOR-722dc38ba432d2571cde0495f3b59d05",
			      "type" : "HOSTMONITOR",
			      "hostRef" : {
			        "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "role_jceks_password",
			          "value" : "2d3ri68c9j2pu125hdbtcj0w9",
			          "sensitive" : true
			        } ]
			      },
			      "roleConfigGroupRef" : {
			        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
			      }
			    }, {
			      "name" : "mgmt-REPORTSMANAGER-722dc38ba432d2571cde0495f3b59d05",
			      "type" : "REPORTSMANAGER",
			      "hostRef" : {
			        "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "role_jceks_password",
			          "value" : "a2zr2akxzarkuivys4vrsjb9t",
			          "sensitive" : true
			        } ]
			      },
			      "roleConfigGroupRef" : {
			        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
			      }
			    }, {
			      "name" : "mgmt-SERVICEMONITOR-722dc38ba432d2571cde0495f3b59d05",
			      "type" : "SERVICEMONITOR",
			      "hostRef" : {
			        "hostId" : "3b3141c4-6a6b-4b07-b34b-c262c662b565"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "role_jceks_password",
			          "value" : "4qlg4vl3xpkpl0odxl3r4zl6i",
			          "sensitive" : true
			        } ]
			      },
			      "roleConfigGroupRef" : {
			        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
			      }
			    } ],
			    "displayName" : "Cloudera Management Service",
			    "roleConfigGroups" : [ {
			      "name" : "mgmt-ACTIVITYMONITOR-BASE",
			      "displayName" : "Activity Monitor Default Group",
			      "roleType" : "ACTIVITYMONITOR",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ ]
			      }
			    }, {
			      "name" : "mgmt-ALERTPUBLISHER-BASE",
			      "displayName" : "Alert Publisher Default Group",
			      "roleType" : "ALERTPUBLISHER",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ ]
			      }
			    }, {
			      "name" : "mgmt-EVENTSERVER-BASE",
			      "displayName" : "Event Server Default Group",
			      "roleType" : "EVENTSERVER",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "event_server_heapsize",
			          "value" : "1062207488",
			          "sensitive" : false
			        } ]
			      }
			    }, {
			      "name" : "mgmt-HOSTMONITOR-BASE",
			      "displayName" : "Host Monitor Default Group",
			      "roleType" : "HOSTMONITOR",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "firehose_heapsize",
			          "value" : "1062207488",
			          "sensitive" : false
			        }, {
			          "name" : "firehose_non_java_memory_bytes",
			          "value" : "1379926016",
			          "sensitive" : false
			        }, {
			          "name" : "role_config_suppression_firehose_heap_size_validator",
			          "value" : "true",
			          "sensitive" : false
			        }, {
			          "name" : "role_config_suppression_firehose_non_java_memory_validator",
			          "value" : "true",
			          "sensitive" : false
			        } ]
			      }
			    }, {
			      "name" : "mgmt-NAVIGATOR-BASE",
			      "displayName" : "Navigator Audit Server Default Group",
			      "roleType" : "NAVIGATOR",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ ]
			      }
			    }, {
			      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
			      "displayName" : "Navigator Metadata Server Default Group",
			      "roleType" : "NAVIGATORMETASERVER",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ ]
			      }
			    }, {
			      "name" : "mgmt-REPORTSMANAGER-BASE",
			      "displayName" : "Reports Manager Default Group",
			      "roleType" : "REPORTSMANAGER",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "headlamp_database_host",
			          "value" : "ip-172-31-30-163.ec2.internal",
			          "sensitive" : false
			        }, {
			          "name" : "headlamp_database_name",
			          "value" : "rman",
			          "sensitive" : false
			        }, {
			          "name" : "headlamp_database_password",
			          "value" : "PassEdgar_1",
			          "sensitive" : true
			        }, {
			          "name" : "headlamp_database_user",
			          "value" : "rman",
			          "sensitive" : false
			        }, {
			          "name" : "headlamp_heapsize",
			          "value" : "1062207488",
			          "sensitive" : false
			        } ]
			      }
			    }, {
			      "name" : "mgmt-SERVICEMONITOR-BASE",
			      "displayName" : "Service Monitor Default Group",
			      "roleType" : "SERVICEMONITOR",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ {
			          "name" : "firehose_heapsize",
			          "value" : "1062207488",
			          "sensitive" : false
			        }, {
			          "name" : "firehose_non_java_memory_bytes",
			          "value" : "1379926016",
			          "sensitive" : false
			        }, {
			          "name" : "role_config_suppression_firehose_heap_size_validator",
			          "value" : "true",
			          "sensitive" : false
			        }, {
			          "name" : "role_config_suppression_firehose_non_java_memory_validator",
			          "value" : "true",
			          "sensitive" : false
			        } ]
			      }
			    }, {
			      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
			      "displayName" : "Telemetry Publisher Default Group",
			      "roleType" : "TELEMETRYPUBLISHER",
			      "base" : true,
			      "serviceRef" : {
			        "serviceName" : "mgmt"
			      },
			      "config" : {
			        "items" : [ ]
			      }
			    } ]
			  },
			  "managerSettings" : {
			    "items" : [ {
			      "name" : "AD_USE_SIMPLE_AUTH",
			      "value" : "false",
			      "sensitive" : false
			    }, {
			      "name" : "CLUSTER_STATS_START",
			      "value" : "10/24/2012 5:20",
			      "sensitive" : false
			    }, {
			      "name" : "KDC_ADMIN_PASSWORD",
			      "value" : "BQIAAABAAAEADUFNQVpPTkFXUy5DT00ADGNsb3VkZXJhLXNjbQAAAAFaHyhcAQAXABAjiZnE0LTsU+wOgXc8oSOOAAAAAQ==",
			      "sensitive" : true
			    }, {
			      "name" : "KDC_ADMIN_USER",
			      "value" : "cloudera-scm@AMAZONAWS.COM",
			      "sensitive" : false
			    }, {
			      "name" : "KDC_HOST",
			      "value" : "ip-172-31-30-163.ec2.internal",
			      "sensitive" : false
			    }, {
			      "name" : "KRB_ENC_TYPES",
			      "value" : "arcfour-hmac",
			      "sensitive" : false
			    }, {
			      "name" : "KRB_MANAGE_KRB5_CONF",
			      "value" : "true",
			      "sensitive" : false
			    }, {
			      "name" : "MAX_RENEW_LIFE",
			      "value" : "604800",
			      "sensitive" : false
			    }, {
			      "name" : "PUBLIC_CLOUD_STATUS",
			      "value" : "ON_PUBLIC_CLOUD",
			      "sensitive" : false
			    }, {
			      "name" : "REMOTE_PARCEL_REPO_URLS",
			      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/",
			      "sensitive" : false
			    }, {
			      "name" : "SECURITY_REALM",
			      "value" : "AMAZONAWS.COM",
			      "sensitive" : false
			    } ]
			  },
			  "allHostsConfig" : {
			    "items" : [ {
			      "name" : "rm_enabled",
			      "value" : "true",
			      "sensitive" : false
			    } ]
			  },
			  "peers" : [ ],
			  "hostTemplates" : {
			    "items" : [ ]
			  }
			}