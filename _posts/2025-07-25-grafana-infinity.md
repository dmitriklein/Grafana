---
title: "Combine different data source types in a single drop-down list by Grafana Infinity"
date: 2025-07-25
tags: [grafana, observability, monitoring, dashboards, time-series]
layout: post
---

## 🚀 Grafana Infinity

How to combine different data source types in a single drop-down list by Grafana Infinity (example):

Type: grafana
Type: dashboard

Chained Variables:
app_name -> app_datasource_name -> app_datasource_type 

===> Infinity Data Source

Plugin / Data Source: Infinity 
Type: yesoreyeram-infinity-datasource
Reference Data
Name: infinity_collection_1
(JSON Collection)

===> Combined Application Names var

Variable: 
Definition: infinity_collection_1 - (infinity) json or (legacy) Collection(*)
Variable type: Query
Name: app_name 
Hide: Variable
Data Source: infinity_collection_1
Selection options: Multi-value; Allow custom values
 "datasource": {"type": "yesoreyeram-infinity-datasource"}
"definition": "Apps_Infinity_Local_Data- (legacy) Collection(
app_name_1,splunkapp,
app_name_2,elkapp,
app_name_3,zabbixapp,
app_name_4,kafkaapp)",

===> Visualization: 
"type": "volkovlabs-variable-panel"


===> Data Source Name Infinity var
Variable: 
"datasource": {"type": "yesoreyeram-infinity-datasource"}
"name": "app_datasource_name",
"definition": "DataSources_Infinity_Local_Data- (legacy) CollectionLookup(
splunkapp,Grafana_Splunk_Data_Source,
elkapp,Grafana_ElasticSearch_Data_Source,
zabbixapp,Grafana_Zabbix_Data_Source,
kafkaapp,Grafana_Kafka_Data_Source,
$app_name)",


===> Data Source Type Infinity var

Variable: 
"datasource": {"type": "yesoreyeram-infinity-datasource"}
"name": "app_datasource_type",
"definition": "DataSourceTypes_Infinity_Local_Data- (legacy) CollectionLookup(
splunkapp,Splunk,
elkapp,Elastic / Kibana,
zabbixapp,Zabbix,
kafkaapp,VictoriaMetrics / Prometheus / Kafka,
$app_name)"

===

---

## 🎯 Overview

Learn how to use Grafana Cloud to monitor, visualize, and take action on your data at your own pace with these hands-on courses.
---

## ⚡ Why Grafana?

- 🧩 Plug-and-play support for diverse data sources
- 🖥️ Customizable dashboards with rich visualization components
- 🔔 Built-in alerting via Slack, email, and more
- 🔍 Explore mode for ad-hoc queries and troubleshooting

---
