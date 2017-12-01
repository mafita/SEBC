[saturn@veroj2 hadoop-mapreduce]$ sudo -u hdfs time hadoop jar hadoop-mapreduce-examples.jar teragen  -Ddfs.blocksize=32M  65536000 /user/saturn/tgen
[sudo] password for saturn: 
17/12/01 18:40:56 INFO client.RMProxy: Connecting to ResourceManager at veroj2.southcentralus.cloudapp.azure.com/10.0.2.5:8032
17/12/01 18:40:57 INFO terasort.TeraGen: Generating 65536000 using 2
17/12/01 18:40:57 INFO mapreduce.JobSubmitter: number of splits:2
17/12/01 18:40:57 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512149582903_0001
17/12/01 18:40:58 INFO impl.YarnClientImpl: Submitted application application_1512149582903_0001
17/12/01 18:40:58 INFO mapreduce.Job: The url to track the job: http://veroj2.southcentralus.cloudapp.azure.com:8088/proxy/application_1512149582903_0001/
17/12/01 18:40:58 INFO mapreduce.Job: Running job: job_1512149582903_0001
17/12/01 18:41:04 INFO mapreduce.Job: Job job_1512149582903_0001 running in uber mode : false
17/12/01 18:41:04 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 18:41:21 INFO mapreduce.Job:  map 19% reduce 0%
17/12/01 18:41:27 INFO mapreduce.Job:  map 33% reduce 0%
17/12/01 18:41:33 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 18:41:39 INFO mapreduce.Job:  map 54% reduce 0%
17/12/01 18:41:57 INFO mapreduce.Job:  map 64% reduce 0%
17/12/01 18:42:03 INFO mapreduce.Job:  map 81% reduce 0%
17/12/01 18:42:09 INFO mapreduce.Job:  map 83% reduce 0%
17/12/01 18:42:21 INFO mapreduce.Job:  map 87% reduce 0%
17/12/01 18:42:23 INFO mapreduce.Job:  map 95% reduce 0%
17/12/01 18:42:25 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 18:42:25 INFO mapreduce.Job: Job job_1512149582903_0001 completed successfully
17/12/01 18:42:25 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=291198
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=170
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters 
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=156097
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=156097
		Total vcore-milliseconds taken by all map tasks=156097
		Total megabyte-milliseconds taken by all map tasks=159843328
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=538
		CPU time spent (ms)=86310
		Physical memory (bytes) snapshot=360652800
		Virtual memory (bytes) snapshot=3193868288
		Total committed heap usage (bytes)=759693312
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000
4.82user 0.32system 1:31.52elapsed 5%CPU (0avgtext+0avgdata 236560maxresident)k
0inputs+1896outputs (0major+73486minor)pagefaults 0swaps
[saturn@veroj2 hadoop-mapreduce]$ 



[saturn@veroj2 hadoop-mapreduce]$ hdfs dfs -ls /user/saturn/tgen
Found 3 items
-rw-r--r--   3 hdfs supergroup          0 2017-12-01 18:42 /user/saturn/tgen/_SUCCESS
-rw-r--r--   3 hdfs supergroup 3276800000 2017-12-01 18:42 /user/saturn/tgen/part-m-00000
-rw-r--r--   3 hdfs supergroup 3276800000 2017-12-01 18:42 /user/saturn/tgen/part-m-00001



[saturn@veroj2 hadoop-mapreduce]$ hadoop fsck -blocks /user/saturn
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://veroj2.southcentralus.cloudapp.azure.com:50070/fsck?ugi=saturn&blocks=1&path=%2Fuser%2Fsaturn
FSCK started by saturn (auth:SIMPLE) from /10.0.2.5 for path /user/saturn at Fri Dec 01 18:47:28 UTC 2017
...Status: HEALTHY
 Total size:	6553600000 B
 Total dirs:	2
 Total files:	3
 Total symlinks:		0
 Total blocks (validated):	196 (avg. block size 33436734 B)
 Minimally replicated blocks:	196 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri Dec 01 18:47:28 UTC 2017 in 7 milliseconds


The filesystem under path '/user/saturn' is HEALTHY
[saturn@veroj2 hadoop-mapreduce]$ 





