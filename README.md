# Assignment8.2

1.	Hadoop yarn 2.x core changes

Hadoop 1
1.	Hadoop 1.x Supports only MapReduce (MR) processing. It does not support non-MR tools.
2.	MR does both processing and cluster resource management.
3.	1.x Has limited scaling of nodes. Limited to 4000 nodes per cluster.
4.	Works on concepts of slots – slots can run either a Map task or a Reduce task only.
5.	A single Namenode to manage the entire namespace.
6.	1.x Has Single-Point-of-Failure (SPOF) – because of single Namenode- and in case of Namenode failure, needs manual intervention to overcome.
7.	MR API is compatible with Hadoop 1x. A program written in Hadoop1 executes in Hadoop1x without any additional files.
8.	1.x Has a limitation to serve as a platform for event processing, streaming and real-time operations.
Hadoop 2
1.	Hadoop 2.x Allows to work in MR as well as other distributed computing models.
2.	YARN (Yet Another Resource Negotiator) does cluster resource management and processing is done using different processing models.
3.	2.x Has better scalability. Scalable up to 10000 nodes per cluster.
4.	Works on concepts of containers i.e. run generic tasks.
5.	Multiple Namenode servers manage multiple namespace.
6.	2.x Has feature to overcome SPOF with a standby Namenode and in case of Namenode failure, it is configured for automatic recovery.
7.	MR API requires additional files for a program written in Hadoop1.x to execute in Hadoop2.x.
8.	Can serve as a platform for a wide variety of data analytics possible to run event processing, streaming and real time operations.

2.	 Explain the difference between MapReduce 1 and MapReduce 2 / Yarn.

MRv1 uses the JobTracker to create and assign tasks to data nodes, which can become a resource bottleneck when the cluster scales out far enough (usually around 4,000 nodes).

MRv2 (aka YARN, "Yet Another Resource Negotiator") has a Resource Manager for each cluster, and each data node runs a Node Manager. For each job, one slave node will act as the Application Master, monitoring resources/tasks, etc.

Hadoop 2.x YARN Benefits
1.	Highly Scalable
2.	Highly Availability
3.	Supports Multiple Programming Models
4.	Supports Multi-Tenancy
5.	Supports Multiple Namespaces
6.	Improved Cluster Utilization
7.	Supports Horizontal Scalability
