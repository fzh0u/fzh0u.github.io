---
title: Understanding RDMA Request Tail Latency
layout: default
nav_order: 1
---

# Understanding RDMA Request Tail Latency

Modern datacenter applications increasingly rely on Remote Direct Memory Access (RDMA) 
to achieve ultra-low latency and high throughput by bypassing the operating system kernel 
and enabling direct data placement into application memory. 

While average RDMA latency can be as low as a few microseconds, tail latency—the high-percentile 
(e.g., 99th or 99.9th) request completion time—remains a critical challenge. 
Unpredictable tail latencies can severely impact the performance of large-scale 
distributed systems, causing request timeouts, head‑of‑line blocking, and degraded user experience.

## Project Goals

This project aims to systematically characterize the sources of tail latency in RDMA operations 
across different transport types (e.g., InfiniBand, RoCE) and network configurations.

- **Identify bottlenecks:** Analyze RDMA tail-latency contributors: network congestion, NIC queuing, etc.
- **Develop models:** Analytical models to capture tail behavior under various loads.
- **Mitigation strategies:** Explore software and hardware techniques (adaptive flow control, scheduling, NIC offloads).
- **Design guidelines:** Deliver best practices for performance-sensitive applications.

## Methodology

- Controlled experiments and microbenchmarks across hardware and configurations.
- Real-world workload traces to ensure practical relevance.
- Tooling for measurement and diagnostics, contributed as open source.

## Expected Outcomes

- Comprehensive taxonomy of RDMA tail-latency bottlenecks
- Open-source measurement tools
- Design guidelines for predictable RDMA-accelerated systems

---

[Results](results.md) | [Measurement Tools](tools.md)
