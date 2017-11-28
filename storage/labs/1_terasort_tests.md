[soaprofessionals@ip-172-31-30-163 ec2-user]$ time hadoop  jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  teragen -Dmapred.map.tasks=4 -Ddfs.block.size=32000000 100000000  /user/soaprofessionals/datos2
17/11/28 20:02:30 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-19-242.ec2.internal/172.31.19.242:8032
17/11/28 20:02:30 INFO terasort.TeraGen: Generating 100000000 using 4
17/11/28 20:02:30 INFO mapreduce.JobSubmitter: number of splits:4
17/11/28 20:02:30 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/11/28 20:02:30 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/11/28 20:02:30 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511894119421_0002
17/11/28 20:02:30 INFO impl.YarnClientImpl: Submitted application application_1511894119421_0002
17/11/28 20:02:30 INFO mapreduce.Job: The url to track the job: http://ip-172-31-19-242.ec2.internal:8088/proxy/application_1511894119421_0002/
17/11/28 20:02:30 INFO mapreduce.Job: Running job: job_1511894119421_0002
17/11/28 20:02:37 INFO mapreduce.Job: Job job_1511894119421_0002 running in uber mode : false
17/11/28 20:02:37 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 20:02:55 INFO mapreduce.Job:  map 15% reduce 0%
17/11/28 20:03:01 INFO mapreduce.Job:  map 23% reduce 0%
17/11/28 20:03:07 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 20:03:13 INFO mapreduce.Job:  map 36% reduce 0%
17/11/28 20:03:19 INFO mapreduce.Job:  map 39% reduce 0%
17/11/28 20:03:25 INFO mapreduce.Job:  map 47% reduce 0%
17/11/28 20:03:31 INFO mapreduce.Job:  map 54% reduce 0%
17/11/28 20:03:37 INFO mapreduce.Job:  map 57% reduce 0%
17/11/28 20:03:43 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 20:03:49 INFO mapreduce.Job:  map 72% reduce 0%
17/11/28 20:03:55 INFO mapreduce.Job:  map 74% reduce 0%
17/11/28 20:04:01 INFO mapreduce.Job:  map 82% reduce 0%
17/11/28 20:04:07 INFO mapreduce.Job:  map 89% reduce 0%
17/11/28 20:04:11 INFO mapreduce.Job:  map 91% reduce 0%
17/11/28 20:04:13 INFO mapreduce.Job:  map 97% reduce 0%
17/11/28 20:04:15 INFO mapreduce.Job:  map 98% reduce 0%
17/11/28 20:04:16 INFO mapreduce.Job:  map 100% reduce 0%
17/11/28 20:04:16 INFO mapreduce.Job: Job job_1511894119421_0002 completed successfully
17/11/28 20:04:16 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=511112
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=380858
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=380858
                Total vcore-milliseconds taken by all map tasks=380858
                Total megabyte-milliseconds taken by all map tasks=389998592
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1182
                CPU time spent (ms)=140690
                Physical memory (bytes) snapshot=786112512
                Virtual memory (bytes) snapshot=6388023296
                Total committed heap usage (bytes)=1717043200
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    1m48.612s
user    0m4.590s
sys     0m0.210s





[soaprofessionals@ip-172-31-30-163 ec2-user]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar  terasort /user/soaprofessionals/datos2 /user/soaprofessionals/salida
17/11/28 20:11:20 INFO terasort.TeraSort: starting
17/11/28 20:11:21 INFO input.FileInputFormat: Total input paths to process : 4
Spent 228ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 235ms
Sampling 10 splits of 316
Making 12 from 100000 sampled records
Computing parititions took 614ms
Spent 851ms computing partitions.
17/11/28 20:11:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-19-242.ec2.internal/172.31.19.242:8032
17/11/28 20:11:22 INFO mapreduce.JobSubmitter: number of splits:316
17/11/28 20:11:22 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1511894119421_0003
17/11/28 20:11:23 INFO impl.YarnClientImpl: Submitted application application_1511894119421_0003
17/11/28 20:11:23 INFO mapreduce.Job: The url to track the job: http://ip-172-31-19-242.ec2.internal:8088/proxy/application_1511894119421_0003/
17/11/28 20:11:23 INFO mapreduce.Job: Running job: job_1511894119421_0003
17/11/28 20:11:28 INFO mapreduce.Job: Job job_1511894119421_0003 running in uber mode : false
17/11/28 20:11:28 INFO mapreduce.Job:  map 0% reduce 0%
17/11/28 20:11:39 INFO mapreduce.Job:  map 1% reduce 0%
17/11/28 20:11:40 INFO mapreduce.Job:  map 2% reduce 0%
17/11/28 20:11:49 INFO mapreduce.Job:  map 3% reduce 0%
17/11/28 20:11:50 INFO mapreduce.Job:  map 4% reduce 0%
17/11/28 20:11:59 INFO mapreduce.Job:  map 5% reduce 0%
17/11/28 20:12:00 INFO mapreduce.Job:  map 6% reduce 0%
17/11/28 20:12:01 INFO mapreduce.Job:  map 7% reduce 0%
17/11/28 20:12:09 INFO mapreduce.Job:  map 8% reduce 0%
17/11/28 20:12:11 INFO mapreduce.Job:  map 9% reduce 0%
17/11/28 20:12:20 INFO mapreduce.Job:  map 10% reduce 0%
17/11/28 20:12:22 INFO mapreduce.Job:  map 11% reduce 0%
17/11/28 20:12:29 INFO mapreduce.Job:  map 12% reduce 0%
17/11/28 20:12:31 INFO mapreduce.Job:  map 13% reduce 0%
17/11/28 20:12:38 INFO mapreduce.Job:  map 14% reduce 0%
17/11/28 20:12:41 INFO mapreduce.Job:  map 15% reduce 0%
17/11/28 20:12:42 INFO mapreduce.Job:  map 16% reduce 0%
17/11/28 20:12:50 INFO mapreduce.Job:  map 17% reduce 0%
17/11/28 20:12:52 INFO mapreduce.Job:  map 18% reduce 0%
17/11/28 20:13:00 INFO mapreduce.Job:  map 19% reduce 0%
17/11/28 20:13:02 INFO mapreduce.Job:  map 20% reduce 0%
17/11/28 20:13:07 INFO mapreduce.Job:  map 21% reduce 0%
17/11/28 20:13:11 INFO mapreduce.Job:  map 22% reduce 0%
17/11/28 20:13:16 INFO mapreduce.Job:  map 23% reduce 0%
17/11/28 20:13:23 INFO mapreduce.Job:  map 24% reduce 0%
17/11/28 20:13:24 INFO mapreduce.Job:  map 25% reduce 0%
17/11/28 20:13:29 INFO mapreduce.Job:  map 26% reduce 0%
17/11/28 20:13:33 INFO mapreduce.Job:  map 27% reduce 0%
17/11/28 20:13:38 INFO mapreduce.Job:  map 28% reduce 0%
17/11/28 20:13:42 INFO mapreduce.Job:  map 29% reduce 0%
17/11/28 20:13:48 INFO mapreduce.Job:  map 30% reduce 0%
17/11/28 20:13:52 INFO mapreduce.Job:  map 31% reduce 0%
17/11/28 20:13:55 INFO mapreduce.Job:  map 32% reduce 0%
17/11/28 20:14:02 INFO mapreduce.Job:  map 34% reduce 0%
17/11/28 20:14:11 INFO mapreduce.Job:  map 35% reduce 0%
17/11/28 20:14:12 INFO mapreduce.Job:  map 36% reduce 0%
17/11/28 20:14:17 INFO mapreduce.Job:  map 37% reduce 0%
17/11/28 20:14:21 INFO mapreduce.Job:  map 38% reduce 0%
17/11/28 20:14:25 INFO mapreduce.Job:  map 39% reduce 0%
17/11/28 20:14:31 INFO mapreduce.Job:  map 40% reduce 0%
17/11/28 20:14:33 INFO mapreduce.Job:  map 41% reduce 0%
17/11/28 20:14:41 INFO mapreduce.Job:  map 42% reduce 0%
17/11/28 20:14:44 INFO mapreduce.Job:  map 43% reduce 0%
17/11/28 20:14:49 INFO mapreduce.Job:  map 44% reduce 0%
17/11/28 20:14:53 INFO mapreduce.Job:  map 45% reduce 0%
17/11/28 20:14:56 INFO mapreduce.Job:  map 46% reduce 0%
17/11/28 20:15:01 INFO mapreduce.Job:  map 47% reduce 0%
17/11/28 20:15:05 INFO mapreduce.Job:  map 48% reduce 0%
17/11/28 20:15:10 INFO mapreduce.Job:  map 49% reduce 0%
17/11/28 20:15:14 INFO mapreduce.Job:  map 50% reduce 0%
17/11/28 20:15:20 INFO mapreduce.Job:  map 51% reduce 0%
17/11/28 20:15:23 INFO mapreduce.Job:  map 52% reduce 0%
17/11/28 20:15:26 INFO mapreduce.Job:  map 53% reduce 0%
17/11/28 20:15:33 INFO mapreduce.Job:  map 54% reduce 0%
17/11/28 20:15:36 INFO mapreduce.Job:  map 55% reduce 0%
17/11/28 20:15:41 INFO mapreduce.Job:  map 56% reduce 0%
17/11/28 20:15:45 INFO mapreduce.Job:  map 57% reduce 0%
17/11/28 20:15:50 INFO mapreduce.Job:  map 58% reduce 0%
17/11/28 20:15:54 INFO mapreduce.Job:  map 59% reduce 0%
17/11/28 20:16:00 INFO mapreduce.Job:  map 60% reduce 0%
17/11/28 20:16:04 INFO mapreduce.Job:  map 61% reduce 0%
17/11/28 20:16:07 INFO mapreduce.Job:  map 62% reduce 0%
17/11/28 20:16:11 INFO mapreduce.Job:  map 63% reduce 0%
17/11/28 20:16:15 INFO mapreduce.Job:  map 64% reduce 0%
17/11/28 20:16:20 INFO mapreduce.Job:  map 65% reduce 0%
17/11/28 20:16:24 INFO mapreduce.Job:  map 66% reduce 0%
17/11/28 20:16:29 INFO mapreduce.Job:  map 67% reduce 0%
17/11/28 20:16:33 INFO mapreduce.Job:  map 68% reduce 0%
17/11/28 20:16:39 INFO mapreduce.Job:  map 69% reduce 0%
17/11/28 20:16:42 INFO mapreduce.Job:  map 70% reduce 0%
17/11/28 20:16:46 INFO mapreduce.Job:  map 71% reduce 0%
17/11/28 20:16:50 INFO mapreduce.Job:  map 72% reduce 0%
17/11/28 20:16:55 INFO mapreduce.Job:  map 73% reduce 0%
17/11/28 20:17:00 INFO mapreduce.Job:  map 74% reduce 0%
17/11/28 20:17:03 INFO mapreduce.Job:  map 75% reduce 0%
17/11/28 20:17:09 INFO mapreduce.Job:  map 76% reduce 0%
17/11/28 20:17:13 INFO mapreduce.Job:  map 77% reduce 0%
17/11/28 20:17:19 INFO mapreduce.Job:  map 78% reduce 0%
17/11/28 20:17:23 INFO mapreduce.Job:  map 79% reduce 0%
17/11/28 20:17:29 INFO mapreduce.Job:  map 80% reduce 0%
17/11/28 20:17:31 INFO mapreduce.Job:  map 81% reduce 0%
17/11/28 20:17:33 INFO mapreduce.Job:  map 82% reduce 0%
17/11/28 20:17:39 INFO mapreduce.Job:  map 83% reduce 0%
17/11/28 20:17:49 INFO mapreduce.Job:  map 84% reduce 0%
17/11/28 20:17:50 INFO mapreduce.Job:  map 84% reduce 5%
17/11/28 20:17:51 INFO mapreduce.Job:  map 84% reduce 7%
17/11/28 20:17:56 INFO mapreduce.Job:  map 85% reduce 7%
17/11/28 20:18:02 INFO mapreduce.Job:  map 86% reduce 7%
17/11/28 20:18:07 INFO mapreduce.Job:  map 87% reduce 7%
17/11/28 20:18:10 INFO mapreduce.Job:  map 88% reduce 7%
17/11/28 20:18:17 INFO mapreduce.Job:  map 89% reduce 7%
17/11/28 20:18:22 INFO mapreduce.Job:  map 90% reduce 7%
17/11/28 20:18:27 INFO mapreduce.Job:  map 91% reduce 7%
17/11/28 20:18:28 INFO mapreduce.Job:  map 91% reduce 8%
17/11/28 20:18:32 INFO mapreduce.Job:  map 92% reduce 8%
17/11/28 20:18:38 INFO mapreduce.Job:  map 93% reduce 8%
17/11/28 20:18:44 INFO mapreduce.Job:  map 94% reduce 8%
17/11/28 20:18:50 INFO mapreduce.Job:  map 95% reduce 8%
17/11/28 20:18:52 INFO mapreduce.Job:  map 96% reduce 8%
17/11/28 20:18:58 INFO mapreduce.Job:  map 97% reduce 8%
17/11/28 20:19:04 INFO mapreduce.Job:  map 98% reduce 8%
17/11/28 20:19:11 INFO mapreduce.Job:  map 99% reduce 8%
17/11/28 20:19:17 INFO mapreduce.Job:  map 100% reduce 8%
17/11/28 20:19:21 INFO mapreduce.Job:  map 100% reduce 14%
17/11/28 20:19:22 INFO mapreduce.Job:  map 100% reduce 17%
17/11/28 20:19:27 INFO mapreduce.Job:  map 100% reduce 19%
17/11/28 20:19:28 INFO mapreduce.Job:  map 100% reduce 20%
17/11/28 20:19:29 INFO mapreduce.Job:  map 100% reduce 25%
17/11/28 20:19:33 INFO mapreduce.Job:  map 100% reduce 28%
17/11/28 20:19:34 INFO mapreduce.Job:  map 100% reduce 29%
17/11/28 20:19:35 INFO mapreduce.Job:  map 100% reduce 34%
17/11/28 20:19:36 INFO mapreduce.Job:  map 100% reduce 39%
17/11/28 20:19:42 INFO mapreduce.Job:  map 100% reduce 42%
17/11/28 20:19:43 INFO mapreduce.Job:  map 100% reduce 46%
17/11/28 20:19:48 INFO mapreduce.Job:  map 100% reduce 49%
17/11/28 20:19:49 INFO mapreduce.Job:  map 100% reduce 53%
17/11/28 20:19:54 INFO mapreduce.Job:  map 100% reduce 56%
17/11/28 20:19:55 INFO mapreduce.Job:  map 100% reduce 61%
17/11/28 20:19:56 INFO mapreduce.Job:  map 100% reduce 64%
17/11/28 20:19:57 INFO mapreduce.Job:  map 100% reduce 65%
17/11/28 20:20:00 INFO mapreduce.Job:  map 100% reduce 70%
17/11/28 20:20:02 INFO mapreduce.Job:  map 100% reduce 73%
17/11/28 20:20:06 INFO mapreduce.Job:  map 100% reduce 78%
17/11/28 20:20:08 INFO mapreduce.Job:  map 100% reduce 82%
17/11/28 20:20:12 INFO mapreduce.Job:  map 100% reduce 84%
17/11/28 20:20:13 INFO mapreduce.Job:  map 100% reduce 86%
17/11/28 20:20:14 INFO mapreduce.Job:  map 100% reduce 90%
17/11/28 20:20:19 INFO mapreduce.Job:  map 100% reduce 93%
17/11/28 20:20:20 INFO mapreduce.Job:  map 100% reduce 95%
17/11/28 20:20:25 INFO mapreduce.Job:  map 100% reduce 97%
17/11/28 20:20:26 INFO mapreduce.Job:  map 100% reduce 98%
17/11/28 20:20:28 INFO mapreduce.Job:  map 100% reduce 99%
17/11/28 20:20:29 INFO mapreduce.Job:  map 100% reduce 100%
17/11/28 20:20:29 INFO mapreduce.Job: Job job_1511894119421_0003 completed successfully
17/11/28 20:20:29 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4428752650
                FILE: Number of bytes written=8813741354
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000046768
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=984
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=24
        Job Counters
                Launched map tasks=316
                Launched reduce tasks=12
                Data-local map tasks=312
                Rack-local map tasks=4
                Total time spent by all maps in occupied slots (ms)=2528065
                Total time spent by all reduces in occupied slots (ms)=719208
                Total time spent by all map tasks (ms)=2528065
                Total time spent by all reduce tasks (ms)=719208
                Total vcore-milliseconds taken by all map tasks=2528065
                Total vcore-milliseconds taken by all reduce tasks=719208
                Total megabyte-milliseconds taken by all map tasks=2588738560
                Total megabyte-milliseconds taken by all reduce tasks=736468992
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4342561788
                Input split bytes=46768
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4342561788
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =3792
                Failed Shuffles=0
                Merged Map outputs=3792
                GC time elapsed (ms)=44860
                CPU time spent (ms)=1499040
                Physical memory (bytes) snapshot=177538183168
                Virtual memory (bytes) snapshot=524878622720
                Total committed heap usage (bytes)=192559448064
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/11/28 20:20:29 INFO terasort.TeraSort: done

real    9m10.050s
user    0m8.969s
sys     0m0.384s