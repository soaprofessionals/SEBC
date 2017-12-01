## The full teragen command and output ##
    time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen -Dmapred.map.tasks=12 -Ddfs.block.size=32000000 65536000  /user/saturn/tgen
## The result of the time command ##
	
	[saturn@ip-172-31-28-107 cloudera-scm-server]$ time hadoop  jar /opt/cloudera/parcels/  CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen -Dmapred.map.tasks=12 -Ddfs  .block.size=32000000 65536000  /user/saturn/tgen
	17/12/01 19:51:38 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-16-2  31.ec2.internal/172.31.16.231:8032
	17/12/01 19:51:39 INFO terasort.TeraSort: Generating 65536000 using 12
	17/12/01 19:51:39 INFO mapreduce.JobSubmitter: number of splits:12
	17/12/01 19:51:39 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Inst  ead, use mapreduce.job.maps
	17/12/01 19:51:39 INFO Configuration.deprecation: dfs.block.size is deprecated. Instea  d, use dfs.blocksize
	17/12/01 19:51:39 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_15121563  85554_0001
	17/12/01 19:51:39 INFO impl.YarnClientImpl: Submitted application application_15121563  85554_0001
	17/12/01 19:51:39 INFO mapreduce.Job: The url to track the job: http://ip-172-31-16-23  1.ec2.internal:8088/proxy/application_1512156385554_0001/
	17/12/01 19:51:39 INFO mapreduce.Job: Running job: job_1512156385554_0001
	17/12/01 19:51:46 INFO mapreduce.Job: Job job_1512156385554_0001 running in uber mode   : false
	17/12/01 19:51:46 INFO mapreduce.Job:  map 0% reduce 0%
	17/12/01 19:51:56 INFO mapreduce.Job:  map 6% reduce 0%
	17/12/01 19:51:59 INFO mapreduce.Job:  map 16% reduce 0%
	17/12/01 19:52:00 INFO mapreduce.Job:  map 19% reduce 0%
	17/12/01 19:52:02 INFO mapreduce.Job:  map 26% reduce 0%
	17/12/01 19:52:03 INFO mapreduce.Job:  map 28% reduce 0%
	17/12/01 19:52:05 INFO mapreduce.Job:  map 33% reduce 0%
	17/12/01 19:52:06 INFO mapreduce.Job:  map 34% reduce 0%
	17/12/01 19:52:08 INFO mapreduce.Job:  map 41% reduce 0%
	17/12/01 19:52:11 INFO mapreduce.Job:  map 48% reduce 0%
	17/12/01 19:52:14 INFO mapreduce.Job:  map 54% reduce 0%
	17/12/01 19:52:17 INFO mapreduce.Job:  map 61% reduce 0%
	17/12/01 19:52:21 INFO mapreduce.Job:  map 67% reduce 0%
	17/12/01 19:52:24 INFO mapreduce.Job:  map 74% reduce 0%
	17/12/01 19:52:27 INFO mapreduce.Job:  map 80% reduce 0%
	17/12/01 19:52:30 INFO mapreduce.Job:  map 86% reduce 0%
	17/12/01 19:52:33 INFO mapreduce.Job:  map 91% reduce 0%
	17/12/01 19:52:36 INFO mapreduce.Job:  map 97% reduce 0%
	17/12/01 19:52:38 INFO mapreduce.Job:  map 100% reduce 0%
	17/12/01 19:52:38 INFO mapreduce.Job: Job job_1512156385554_0001 completed successfull  y
	17/12/01 19:52:38 INFO mapreduce.Job: Counters: 31
	File System Counters
	FILE: Number of bytes read=0
	FILE: Number of bytes written=1479578
	FILE: Number of read operations=0
	FILE: Number of large read operations=0
	FILE: Number of write operations=0
	HDFS: Number of bytes read=1025
	HDFS: Number of bytes written=6553600000
	HDFS: Number of read operations=48
	HDFS: Number of large read operations=0
	HDFS: Number of write operations=24
	Job Counters
	Launched map tasks=12
	Other local map tasks=12
	Total time spent by all maps in occupied slots (ms)=552596
	Total time spent by all reduces in occupied slots (ms)=0
	Total time spent by all map tasks (ms)=552596
	Total vcore-seconds taken by all map tasks=552596
	Total megabyte-seconds taken by all map tasks=565858304
	Map-Reduce Framework
	Map input records=65536000
	Map output records=65536000
	Input split bytes=1025
	Spilled Records=0
	Failed Shuffles=0
	Merged Map outputs=0
	GC time elapsed (ms)=1804
	CPU time spent (ms)=136430
	Physical memory (bytes) snapshot=3956989952
	Virtual memory (bytes) snapshot=19164942336
	Total committed heap usage (bytes)=6608125952
	org.apache.hadoop.examples.terasort.TeraGen$Counters
	CHECKSUM=140750829423462787
	File Input Format Counters
	Bytes Read=0
	File Output Format Counters
	Bytes Written=6553600000
	
	real1m1.579s
	user0m4.396s
	sys 0m0.246s






## The command and output of hdfs dfs -ls /user/saturn/tgen ##
	
	[saturn@ip-172-31-28-107 cloudera-scm-server]$ hdfs dfs -ls /user/saturn/tgen
	Found 13 items
	-rw-r--r--   3 saturn saturn  0 2017-12-01 19:52 /user/saturn/tgen/_SUCCESS
	-rw-r--r--   3 saturn saturn  546133400 2017-12-01 19:52 /user/saturn/tgen/part-m-00000
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00001
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00002
	-rw-r--r--   3 saturn saturn  546133400 2017-12-01 19:52 /user/saturn/tgen/part-m-00003
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00004
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00005
	-rw-r--r--   3 saturn saturn  546133400 2017-12-01 19:52 /user/saturn/tgen/part-m-00006
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00007
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00008
	-rw-r--r--   3 saturn saturn  546133400 2017-12-01 19:52 /user/saturn/tgen/part-m-00009
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00010
	-rw-r--r--   3 saturn saturn  546133300 2017-12-01 19:52 /user/saturn/tgen/part-m-00011




## The command and output of hadoop fsck -blocks /user/saturn ##

	[saturn@ip-172-31-28-107 cloudera-scm-server]$ hadoop fsck -blocks /user/saturn
	DEPRECATED: Use of this script to execute hdfs command is deprecated.
	Instead use the hdfs command for it.
	
	Connecting to namenode via http://ip-172-31-16-231.ec2.internal:50070
	FSCK started by saturn (auth:SIMPLE) from /172.31.28.107 for path /user/saturn at Fri Dec 01 19:56:12 UTC 2017
	.............Status: HEALTHY
	 Total size:6553600000 B
	 Total dirs:3
	 Total files:   13
	 Total symlinks:0
	 Total blocks (validated):  216 (avg. block size 30340740 B)
	 Minimally replicated blocks:   216 (100.0 %)
	 Over-replicated blocks:0 (0.0 %)
	 Under-replicated blocks:   0 (0.0 %)
	 Mis-replicated blocks: 0 (0.0 %)
	 Default replication factor:3
	 Average block replication: 3.0
	 Corrupt blocks:0
	 Missing replicas:  0 (0.0 %)
	 Number of data-nodes:  3
	 Number of racks:   1
	FSCK ended at Fri Dec 01 19:56:12 UTC 2017 in 12 milliseconds
	
	
	The filesystem under path '/user/saturn' is HEALTHY
