
[root@ip-172-31-30-163 ec2-user]# chmod 777 YARNtest.sh
[root@ip-172-31-30-163 ec2-user]# clear
[root@ip-172-31-30-163 ec2-user]#  HADOOP_USER_NAME=hdfs ./YARNtest.sh
Testing loop started on Tue Nov 28 23:02:38 UTC 2017
8 conteiners
1 reducers
memoria 512 1024

real    1m34.738s
user    0m4.609s
sys     0m0.209s

real    2m41.090s
user    0m6.737s
sys     0m0.241s
Deleted /results/tg-10GB-8-1-512
Deleted /results/ts-10GB-8-1-512

real    3m9.047s
user    0m4.773s
sys     0m0.253s

real    2m37.755s
user    0m6.344s
sys     0m0.228s
Deleted /results/tg-10GB-8-1-1024
Deleted /results/ts-10GB-8-1-1024
Testing loop ended on Tue Nov 28 23:12:49 UTC 2017
[root@ip-172-31-30-163 ec2-user]#


HADOOP_USER_NAME=hdfs ./YARNtest.sh
Testing loop started on Tue Nov 28 23:20:54 UTC 2017
4 conteiners
2 reducers
memoria 512 1024

real    1m9.618s
user    0m4.614s
sys     0m0.224s

real    2m37.954s
user    0m6.749s
sys     0m0.268s
Deleted /results/tg-10GB-4-2-512
Deleted /results/ts-10GB-4-2-512

real    1m12.532s
user    0m4.650s
sys     0m0.223s

real    2m29.982s
user    0m7.129s
sys     0m0.263s
Deleted /results/tg-10GB-4-2-1024
Deleted /results/ts-10GB-4-2-1024
Testing loop ended on Tue Nov 28 23:28:33 UTC 2017
