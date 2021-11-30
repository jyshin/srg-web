---
layout: seminar
talk-title: Efficient Strong Scaling Through Burst Parallel Training
speaker: Seo Jin Park
affiliation: MIT
speaker-webpage:
date: Nov 19, 2021
day: Friday
time: 11:00 am 
location: ISEC 142
online: YES
---

**Abstract:**

As emerging deep neural network (DNN) models continue to grow in size, using large GPU clusters to train DNNs is becoming an essential requirement to achieving acceptable training times. In this paper, we consider the case where future increases in cluster size will cause the global batch size that can be used to train models to reach a fundamental limit: beyond a certain point, larger global batch sizes cause sample efficiency to degrade, increasing overall time to accuracy. As a result, to achieve further improvements in training performance, we must instead consider ``strong scaling'' strategies that hold the global batch size constant and allocate smaller batches to each GPU. Unfortunately, this makes it significantly more difficult to use cluster resources efficiently.

I present DeepPool, a system that addresses this efficiency challenge through two key ideas. First, Burst parallelism allocates large numbers of GPUs to foreground jobs in bursts to exploit the unevenness in parallelism across layers. Second, GPU multiplexing prioritizes throughput for foreground training jobs, while packing in background training jobs to reclaim underutilized GPU resources, thereby improving cluster-wide utilization. Together, these two ideas enable DeepPool to deliver a 2.2 - 2.4x improvement in total cluster throughput over standard data parallelism with a single task when the cluster scale is large.
 
**Bio:**

Seo Jin Park is a postdoc associate at MIT CSAIL, advised by Mohammad Alizadeh. He received PhD in Computer Science in 2019 from Stanford University with John Ousterhout. His research focuses on making cluster-scale parallel systems efficient so that big data applications (e.g., DNN training, analytics) can run 100--1000x faster on the public cloud. Other areas of research are improving blockchain throughput under network bandwidth variability, removing overheads of consistent replication, and building tools for debugging tail latencies. Before coming to Stanford for PhD, he previously received M.Eng. in EECS and B.S. in Computer Science and Mathematics from MIT in 2013.
