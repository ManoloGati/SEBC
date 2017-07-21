Challenge 3 - Install CDH 5.11.1

[root@ip-172-31-43-231 /]# sudo -u hdfs hdfs dfs -ls /user/                     Found 7 items
drwxr-xr-x   - haley  haley           0 2017-07-21 18:18 /user/haley
drwxrwxrwx   - mapred hadoop          0 2017-07-21 17:13 /user/history
drwxrwxr-t   - hive   hive            0 2017-07-21 17:14 /user/hive
drwxrwxr-x   - hue    hue             0 2017-07-21 17:14 /user/hue
drwxrwxr-x   - oozie  oozie           0 2017-07-21 17:18 /user/oozie
drwxr-xr-x   - saturn saturn          0 2017-07-21 18:17 /user/saturn
drwxr-x--x   - spark  spark           0 2017-07-21 18:07 /user/spark


http://52.34.220.141:7180/api/v14/hosts

{
  "items" : [ {
    "hostId" : "9acea6a0-4925-46c9-91f3-3db27a2015a9",
    "ipAddress" : "172.31.34.102",
    "hostname" : "ip-172-31-34-102.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/hostRedirect/9acea6a0-4925-46c9-91f3-3db27a2015a9",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31185281024
  }, {
    "hostId" : "b39d7a7c-cea3-47eb-ac36-32908707603e",
    "ipAddress" : "172.31.41.99",
    "hostname" : "ip-172-31-41-99.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/hostRedirect/b39d7a7c-cea3-47eb-ac36-32908707603e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31185281024
  }, {
    "hostId" : "532db0d4-345c-4bcb-a6d7-dc0d4968579d",
    "ipAddress" : "172.31.43.231",
    "hostname" : "ip-172-31-43-231.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/hostRedirect/532db0d4-345c-4bcb-a6d7-dc0d4968579d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31185281024
  }, {
    "hostId" : "d103193a-de73-42fe-99c3-2844342614e4",
    "ipAddress" : "172.31.44.49",
    "hostname" : "ip-172-31-44-49.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/hostRedirect/d103193a-de73-42fe-99c3-2844342614e4",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31185281024
  }, {
    "hostId" : "5cbb967a-02f1-4c07-80bd-4f190b042c78",
    "ipAddress" : "172.31.46.76",
    "hostname" : "ip-172-31-46-76.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/hostRedirect/5cbb967a-02f1-4c07-80bd-4f190b042c78",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 8,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 31185281024
  } ]
}


http://52.34.220.141:7180/api/v8/clusters/ManoloGati/services

{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  }, {
    "name" : "spark_on_yarn",
    "type" : "SPARK_ON_YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-41-99.us-west-2.compute.internal:7180/cmf/serviceRedirect/spark_on_yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Spark"
  } ]
}