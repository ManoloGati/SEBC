Challenge 4 - HDFS Testing

# sudo -u saturn time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.job.maps=12 -Dmapreduce.map.memory.mb=32 -Dmapreduce.map.java.opts.max.heap=512 65536000 /user/saturn/tgen

17/07/21 19:22:36 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-44-49.us-west-2.compute.internal/172.31.44.49:8032
17/07/21 19:22:37 INFO terasort.TeraGen: Generating 65536000 using 12
17/07/21 19:22:37 INFO mapreduce.JobSubmitter: number of splits:12
17/07/21 19:22:37 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1500660468630_0001
17/07/21 19:22:38 INFO impl.YarnClientImpl: Submitted application application_1500660468630_0001
17/07/21 19:22:38 INFO mapreduce.Job: The url to track the job: http://ip-172-31-44-49.us-west-2.compute.internal:8088/proxy/application_1500660468630_0001/
17/07/21 19:22:38 INFO mapreduce.Job: Running job: job_1500660468630_0001
17/07/21 19:22:45 INFO mapreduce.Job: Job job_1500660468630_0001 running in uber mode : false
17/07/21 19:22:45 INFO mapreduce.Job:  map 0% reduce 0%
17/07/21 19:23:03 INFO mapreduce.Job:  map 8% reduce 0%
17/07/21 19:23:05 INFO mapreduce.Job:  map 24% reduce 0%
17/07/21 19:23:06 INFO mapreduce.Job:  map 33% reduce 0%
17/07/21 19:23:10 INFO mapreduce.Job:  map 35% reduce 0%
17/07/21 19:23:12 INFO mapreduce.Job:  map 45% reduce 0%
17/07/21 19:23:13 INFO mapreduce.Job:  map 49% reduce 0%
17/07/21 19:23:16 INFO mapreduce.Job:  map 51% reduce 0%
17/07/21 19:23:17 INFO mapreduce.Job:  map 57% reduce 0%
17/07/21 19:23:18 INFO mapreduce.Job:  map 63% reduce 0%
17/07/21 19:23:19 INFO mapreduce.Job:  map 67% reduce 0%
17/07/21 19:23:22 INFO mapreduce.Job:  map 70% reduce 0%
17/07/21 19:23:23 INFO mapreduce.Job:  map 75% reduce 0%
17/07/21 19:23:24 INFO mapreduce.Job:  map 82% reduce 0%
17/07/21 19:23:25 INFO mapreduce.Job:  map 86% reduce 0%
17/07/21 19:23:29 INFO mapreduce.Job:  map 90% reduce 0%
17/07/21 19:23:30 INFO mapreduce.Job:  map 96% reduce 0%
17/07/21 19:23:31 INFO mapreduce.Job:  map 100% reduce 0%
17/07/21 19:23:32 INFO mapreduce.Job: Job job_1500660468630_0001 completed successfully
17/07/21 19:23:32 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1534010
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
                Total time spent by all maps in occupied slots (ms)=495881
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=495881
                Total vcore-milliseconds taken by all map tasks=495881
                Total megabyte-milliseconds taken by all map tasks=507782144
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=1025
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=66035
                CPU time spent (ms)=280030
                Physical memory (bytes) snapshot=1521127424
                Virtual memory (bytes) snapshot=8859484160
                Total committed heap usage (bytes)=289406976
                Peak Map Physical memory (bytes)=135323648
                Peak Map Virtual memory (bytes)=749031424
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000
4.96user 0.26system 0:57.80elapsed 9%CPU (0avgtext+0avgdata 244492maxresident)k
0inputs+1008outputs (0major+34892minor)pagefaults 0swaps

[root@ip-172-31-43-231 hadoop-0.20-mapreduce]# sudo -u hdfs hdfs dfs -ls /user/saturn/tgen
Found 13 items
-rw-r--r--   3 saturn saturn          0 2017-07-21 19:23 /user/saturn/tgen/_SUCCESS
-rw-r--r--   3 saturn saturn  546133400 2017-07-21 19:23 /user/saturn/tgen/part-m-00000
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00001
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00002
-rw-r--r--   3 saturn saturn  546133400 2017-07-21 19:23 /user/saturn/tgen/part-m-00003
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00004
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00005
-rw-r--r--   3 saturn saturn  546133400 2017-07-21 19:23 /user/saturn/tgen/part-m-00006
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00007
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00008
-rw-r--r--   3 saturn saturn  546133400 2017-07-21 19:23 /user/saturn/tgen/part-m-00009
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00010
-rw-r--r--   3 saturn saturn  546133300 2017-07-21 19:23 /user/saturn/tgen/part-m-00011

[root@ip-172-31-43-231 hadoop-0.20-mapreduce]# sudo -u hdfs hadoop fsck -blocks /user/saturn
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-41-99.us-west-2.compute.internal:50070
FSCK started by hdfs (auth:SIMPLE) from /172.31.43.231 for path /user/saturn at Fri Jul 21 19:26:26 UTC 2017
.............Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    3
 Total files:   13
 Total symlinks:                0
 Total blocks (validated):      60 (avg. block size 109226666 B)
 Minimally replicated blocks:   60 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri Jul 21 19:26:26 UTC 2017 in 6 milliseconds


The filesystem under path '/user/saturn' is HEALTHY



