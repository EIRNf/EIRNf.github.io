---
title: "Split gRPC: An Isolation Architecture for RPC Stacks on SmartNICs"
date: 2023-08-17
---

It was an absolute pleasure to attend the Computational IO Workshop. Lots of great talks and great work presented! 


[Talk + Slides](https://skyhookdm.github.io/talks/20230817/esteban.ramos/)


### Talk Blurb
Remote procedure calls are a major contributor to performance variance in distributed systems due to lack of isolation and contention on shared resources. In this talk, I will introduce the novel architecture we built to address this problem, and cover our experience in implementing a prototype over gRPC with an emphasis on the communication layer between a host CPU and the SmartNIC. The basic idea is to partition RPC applications into two communicating components: one dedicated to user-implemented business logic, and one dedicated to RPC infrastructure processing. The infrastructure process can be run on a dedicated core or on a smart NIC (e.g., IPU or DPU), providing effective physical isolation and predictable performance. An evaluation of a proof-of-concept prototype shows that the split architecture adds modest overhead for average case latency, but allows for lower latency and and higher throughput under host CPU load.

