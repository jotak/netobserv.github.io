---
layout: :theme/post
title: "..."
description: "..."
tags: TODO
authors: [jotak]
---

_Thanks to: ..._

- Quick call-out of previous filtering blog
- Present new feature
- When using one or another?
- Sampling, the good bad and ugly
- Normalization


=> Current promQL:
```
sum(rate(netobserv_workload_egress_bytes_total{K8S_FlowLayer="app",SrcK8S_Namespace!=""}[2m])) by (SrcK8S_Namespace,DstK8S_Namespace) * on() group_left avg(netobserv_agent_sampling_rate)
```
