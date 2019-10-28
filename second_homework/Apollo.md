# Apollo: Scalable and Coordinated Scheduling for Cloud-Scale Computing

## Introduction

Apollo is a highly scalable and coordinated cluster scheduling framework developed by Microsoft. It is deployed on Microsoft's production clusters and can run efficiently on tens of thousands of machines and schedule thousands of operations. It uses a distributed framework and uses a shared cluster state to give each scheduler a cluster perspective. Apollo is powerful enough to take advantage of idle system resources while providing guaranteed resources when needed.

## Challenges

Minimize job latency while maximizing cluster utilization.

1. How to make optimal scheduling decisions at full production scale.

2. Make optimal scheduling decisions for a complex workload.

3. Maximize utilization while maintaining performance guarantees with a dynamic workload.

## The Apollo Framework

### Overview

Apollo adopts a distributed and coordinated architecture. There is one scheduler per job each making high quality decisions independently informed by global information.
The distributed architectures scales by allowing schedulers to make independent decisions with global coordination.

### Load Representation

Apollo represents the load using a wait-time matrix. It represents the expected wait time to obtain resource of a certain size. The wait time matrix allows to reason about future resource availability.

### Estimation of Jobs

Apollo minimizes the estimated task completion time by using the following formula: 

*E = I + W + R*

E: Estimated task completion time

I: Initializatin time

W: Wait time

R: Runtime

### Correction Mechanisms

Cluster is dynamic. Schedulers can have conflicts. Apollo defers the correction of conflict. The correction mechanisms allows Apollo to handle cluster dynamics. Apollo re-evaluates prior decisions. Triggers a duplicate if the decision isn't optimal with up to date information.

### Opportunistic Scheduling

Opportunistic scheduling maximizes utilization by using the remaining capacity and dispatching more than the resource allocation. Tasks can be preempted or terminated. Meanwhile, Tasks can be upgraded. Opportunistic scheduling allows Apollo to maximize utilization.

### Random Queuing
Since Apollo is a distributed system, different job managers may schedule tasks to the same server. In order to avoid this situation, Apollo will add a small random number to the estimated end time, reducing the probability of scheduling to the same server.

## Conclusion

Apollo is a loosely coordinated distributed architecture deployed to clusters with over 20,000 servers. The high quality scheduling minimizes task completion time and has consistent performance. It maximizes resource utilization with opportunistic scheduling and other techniques.
