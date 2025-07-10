---
layout: post
title: "Mastering Observability with Style"
date: 2025-07-09
categories: observability tools
tags: [grafana, prometheus, opentelemetry]
excerpt: "A visually enhanced walkthrough of observability tooling."
---

![Observability Banner](assets/images/MyObservabilityLogo3.png)

## 🎯 Overview

In this post, we explore how to set up a sleek observability stack using:

- ✅ **Prometheus** for metrics
- 🔍 **Loki** for logs
- 🧵 **OpenTelemetry** for distributed tracing

## 💡 Dashboard Tips

```yaml
scrape_configs:
  - job_name: 'node'
    static_configs:
      - targets: ['localhost:9100']
