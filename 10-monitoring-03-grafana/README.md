# Домашнее задание к занятию "10.03. Grafana"

## Обязательные задания

### Задание 1

![Screenshot from 2022-04-27 17-23-01](https://user-images.githubusercontent.com/88886716/165698846-2ab6edd0-acf3-4905-8fe2-917c3d6386ed.png)

### Задание 2

![Screenshot from 2022-04-28 10-05-01](https://user-images.githubusercontent.com/88886716/165698983-1a40cc63-e09f-4f16-96df-3d3f7af9a3ca.png)

```
node_filesystem_avail_bytes{job="nodeexporter"}

node_load1{job='nodeexporter'}
node_load5{job='nodeexporter'}
node_load15{job='nodeexporter'}

node_memory_MemFree_bytes{job='nodeexporter'}

100 – rate(node_cpu_seconds_total{job="nodeexporter",mode='idle'}[1m])*100
```

### Задание 3

![Screenshot from 2022-04-28 10-14-23](https://user-images.githubusercontent.com/88886716/165699248-45df2452-e947-4ec9-98f6-848d6b202464.png)

### Задание 4
```
{
"annotations": {
"list": [
{
"builtIn": 1,
"datasource": "-- Grafana --",
"enable": true,
"hide": true,
"iconColor": "rgba(0, 211, 255, 1)",
"name": "Annotations & Alerts",
"type": "dashboard"
}
]
},
"editable": true,
"gnetId": null,
"graphTooltip": 0,
"id": 1,
"links": [],
"panels": [
{
"aliasColors": {},
"bars": false,
"dashLength": 10,
"dashes": false,
"datasource": null,
"fieldConfig": {
"defaults": {
"custom": {}
},
"overrides": []
},
"fill": 1,
"fillGradient": 0,
"gridPos": {
"h": 8,
"w": 12,
"x": 0,
"y": 0
},
"hiddenSeries": false,
"id": 8,
"legend": {
"avg": false,
"current": false,
"max": false,
"min": false,
"show": true,
"total": false,
"values": false
},
"lines": true,
"linewidth": 1,
"nullPointMode": "null",
"options": {
"alertThreshold": true
},
"percentage": false,
"pluginVersion": "7.4.0",
"pointradius": 2,
"points": false,
"renderer": "flot",
"seriesOverrides": [],
"spaceLength": 10,
"stack": false,
"steppedLine": false,
"targets": [
{
"expr": "node_filesystem_avail_bytes{job=\"nodeexporter\"}",
"interval": "",
"legendFormat": "",
"refId": "A"
}
],
"thresholds": [
{
"$$hashKey": "object:618",
"colorMode": "ok",
"fill": true,
"line": true,
"op": "lt",
"value": 5000000000,
"yaxis": "left"
}
],
"timeFrom": null,
"timeRegions": [],
"timeShift": null,
"title": "FreeSpace",
"tooltip": {
"shared": true,
"sort": 0,
"value_type": "individual"
},
"type": "graph",
"xaxis": {
"buckets": null,
"mode": "time",
"name": null,
"show": true,
"values": []
},
"yaxes": [
{
"$$hashKey": "object:702",
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
},
{
"$$hashKey": "object:703",
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
}
],
"yaxis": {
"align": false,
"alignLevel": null
}
},
{
"aliasColors": {},
"bars": false,
"dashLength": 10,
"dashes": false,
"datasource": null,
"fieldConfig": {
"defaults": {
"custom": {}
},
"overrides": []
},
"fill": 1,
"fillGradient": 0,
"gridPos": {
"h": 8,
"w": 12,
"x": 12,
"y": 0
},
"hiddenSeries": false,
"id": 4,
"legend": {
"avg": false,
"current": false,
"max": false,
"min": false,
"show": true,
"total": false,
"values": false
},
"lines": true,
"linewidth": 1,
"nullPointMode": "null",
"options": {
"alertThreshold": true
},
"percentage": false,
"pluginVersion": "7.4.0",
"pointradius": 2,
"points": false,
"renderer": "flot",
"seriesOverrides": [],
"spaceLength": 10,
"stack": false,
"steppedLine": false,
"targets": [
{
"expr": "node_load1{job='nodeexporter'}",
"interval": "",
"legendFormat": "",
"refId": "A"
},
{
"expr": "node_load5{job='nodeexporter'}",
"hide": false,
"interval": "",
"legendFormat": "",
"refId": "B"
},
{
"expr": "node_load15{job='nodeexporter'}",
"hide": false,
"interval": "",
"legendFormat": "",
"refId": "C"
}
],
"thresholds": [
{
"$$hashKey": "object:775",
"colorMode": "critical",
"fill": true,
"line": true,
"op": "gt",
"value": 3,
"yaxis": "left"
}
],
"timeFrom": null,
"timeRegions": [],
"timeShift": null,
"title": "Load_1/5/15",
"tooltip": {
"shared": true,
"sort": 0,
"value_type": "individual"
},
"type": "graph",
"xaxis": {
"buckets": null,
"mode": "time",
"name": null,
"show": true,
"values": []
},
"yaxes": [
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
},
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
}
],
"yaxis": {
"align": false,
"alignLevel": null
}
},
{
"aliasColors": {},
"bars": false,
"dashLength": 10,
"dashes": false,
"datasource": null,
"fieldConfig": {
"defaults": {
"custom": {}
},
"overrides": []
},
"fill": 1,
"fillGradient": 0,
"gridPos": {
"h": 8,
"w": 12,
"x": 0,
"y": 8
},
"hiddenSeries": false,
"id": 6,
"legend": {
"avg": false,
"current": false,
"max": false,
"min": false,
"show": true,
"total": false,
"values": false
},
"lines": true,
"linewidth": 1,
"nullPointMode": "null",
"options": {
"alertThreshold": true
},
"percentage": false,
"pluginVersion": "7.4.0",
"pointradius": 2,
"points": false,
"renderer": "flot",
"seriesOverrides": [],
"spaceLength": 10,
"stack": false,
"steppedLine": false,
"targets": [
{
"expr": "node_memory_MemFree_bytes{job='nodeexporter'}",
"interval": "",
"legendFormat": "",
"refId": "A"
}
],
"thresholds": [
{
"$$hashKey": "object:813",
"colorMode": "critical",
"fill": true,
"line": true,
"op": "gt",
"value": 250000000,
"yaxis": "left"
}
],
"timeFrom": null,
"timeRegions": [],
"timeShift": null,
"title": "MemFree",
"tooltip": {
"shared": true,
"sort": 0,
"value_type": "individual"
},
"type": "graph",
"xaxis": {
"buckets": null,
"mode": "time",
"name": null,
"show": true,
"values": []
},
"yaxes": [
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
},
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
}
],
"yaxis": {
"align": false,
"alignLevel": null
}
},
{
"aliasColors": {},
"bars": false,
"dashLength": 10,
"dashes": false,
"datasource": null,
"fieldConfig": {
"defaults": {
"color": {},
"custom": {},
"thresholds": {
"mode": "absolute",
"steps": []
}
},
"overrides": []
},
"fill": 1,
"fillGradient": 0,
"gridPos": {
"h": 8,
"w": 12,
"x": 12,
"y": 8
},
"hiddenSeries": false,
"id": 2,
"legend": {
"avg": false,
"current": false,
"max": false,
"min": false,
"show": true,
"total": false,
"values": false
},
"lines": true,
"linewidth": 1,
"nullPointMode": "null",
"options": {
"alertThreshold": true
},
"percentage": false,
"pluginVersion": "7.4.0",
"pointradius": 2,
"points": false,
"renderer": "flot",
"seriesOverrides": [],
"spaceLength": 10,
"stack": false,
"steppedLine": false,
"targets": [
{
"expr": "100 - rate(node_cpu_seconds_total{job=\"nodeexporter\",mode='idle'}[1m])*100",
"interval": "",
"legendFormat": "",
"refId": "A"
}
],
"thresholds": [
{
"$$hashKey": "object:851",
"colorMode": "critical",
"fill": true,
"line": true,
"op": "gt",
"value": 60,
"yaxis": "left"
}
],
"timeFrom": null,
"timeRegions": [],
"timeShift": null,
"title": "CPU",
"tooltip": {
"shared": true,
"sort": 0,
"value_type": "individual"
},
"type": "graph",
"xaxis": {
"buckets": null,
"mode": "time",
"name": null,
"show": true,
"values": []
},
"yaxes": [
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
},
{
"format": "short",
"label": null,
"logBase": 1,
"max": null,
"min": null,
"show": true
}
],
"yaxis": {
"align": false,
"alignLevel": null
}
}
],
"refresh": "5s",
"schemaVersion": 27,
"style": "dark",
"tags": [],
"templating": {
"list": []
},
"time": {
"from": "now-6h",
"to": "now"
},
"timepicker": {},
"timezone": "",
"title": "My board",
"uid": "0ACs-Uwnk",
"version": 6
}
```
