<link rel="stylesheet" href="{{ '/assets/css/style.css' | https://github.com/dmitriklein/Grafana }}">
---
layout: post
title: "Why Grafana Matters"
date: 2025-07-09
categories: observability cloud
tags: [grafana, prometheus, opentelemetry]
excerpt: "A quick dive into why observability is essential in modern cloud-native systems."
---

I strongly endorse the use of the Grafana:
- custom variables and business variables. They function exceptionally well in drop-down lists and menus integrated within panels/visualizations.
- chained variables. They function exceptionally well for smart data selecting from Elastic and Splunk mixed data sources.
- Infinity plugin and data source. They function exceptionally well for generating small-scale local and remote (http) data collections. As a result, the Infinity data source can be effortlessly integrated into Grafana visualizations’ drop-down lists.
