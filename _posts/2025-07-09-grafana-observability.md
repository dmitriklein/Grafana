---
layout: post
title: "Grafana Observability Tips"
date: 2025-07-09 20:30:00 -0600
categories: [grafana, observability]
---
## Why Grafana Rocks

Grafana makes it easy to visualize metrics from Prometheus, Loki, and more.

```promql
rate(node_cpu_seconds_total[1m])
