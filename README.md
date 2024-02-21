# ABS Platform for Edge-Cloud Workload Migration

The repository contains the ABS implementation of the SEAWALL platform enabling seamless orchestration of workloads in the edge-cloud continuum so that the latency of the alerting service is minimized requirement of the processing task is continuously met, while taking into account the constrained resources of the edge servers. Moreover, to test the accuracy of the ABS implementation, we reproduce the small-case industrial testbed presented in [1]. Differently from [1], here the deployment orchestrations, performing service migration, are automatically synthesized using the SmartDeployer tool [2], starting from declarative annotation describing service properties (e.g., resource required, functional dependencies, etc.).

## ABS Implementation

## Experimental Results


<img src="images/readme/rw_latency.png" alt="Real-world implementation" width="400"/> <img src="images/readme/abs_latency.png" alt="ABS implementation" width="400"/>

<img src="images/readme/rw_byte.png" alt="Real-world implementation" width="400"/> <img src="images/readme/abs_byte.png" alt="ABS implementation" width="400"/>


| | Latency-based policy (Real-world) | Byte-based policy (Real-world)| Latency-based policy (ABS) | Byte-based policy (ABS)|
|-----------------|-----------------|-----------------|-----------------|-----------------|
| Pipeline 1: swaps |11 | 4 | 8 | 5 |
| Pipeline 1: avg latency | 1.8s | 1.8s | 2s | 1.7s |
| Pipeline 2: swaps | 10 | 3 | 7 | 4 |
| Pipeline 2: avg latency | 1.8s | 1.8s | 2.1s | 2.1s |
| Pipeline 3: swaps | 8 | 4 | 8 | 4 |
| Pipeline 3: avg latency | 2s | 1.9s | 1.8s | 1.7s |


[1] [Low-Latency Anomaly Detection on the Edge-Cloud Continuum for Industry 4.0 Applications: The SEAWALL Case Study](https://ieeexplore.ieee.org/abstract/document/9945851)
[2] [SmartDeployer tool](https://github.com/jacopoMauro/abs_deployer)
