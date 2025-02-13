---
title: "查看计算节点详情"
description: 本小节主要介绍青立方® 超融合易捷版 查看计算节点详情。 
keyword: 青立方® 超融合易捷版，查看计算节点详情
weight: 20
collapsible: false
draft: false
---


计算节点详情页面，主要展示当前计算节点的物理资源与虚拟资源的使用情况、健康状况和系统性能等监控信息。

本小节主要介绍查看节点详情。

## 前提条件

- 已登录 Express。

## 操作步骤

1. 选择**物理资源** > **管理节点**，进入计算节点管理页面。
2. 点击目标节点区域，进入计算节点详情页面。
   
### 资源监控

在**资源监控**页面，可查看当前计算节点的 CPU、内存、交换分区使用率等监控信息，以及硬盘的使用率、IOPS、吞吐量等性能指标的监控。通常情况下，吞吐量越大、响应时间越快则磁盘性能就越高。

- **监控周期**：监控指标的时间范围，目前分别支持：最近6小时、最近一天、最近两周、最近一个月等。

- **查看监控数据**：将鼠标悬浮于某个图表上，会自动展开图表上的所有监控数据，如下图，点击图表上的一个时间点，下方自动展开资源详情信息，可查看具体数据。

- 点击监控图表的右上角放大图标即可放大图表。

![资源监控](../../../_images/node_monitoring.png)

![硬盘监控](../../../_images/node_monitoring_2.png)

### 网卡监控

在**网卡监控**页面，目前网卡监控提供物理主机网卡的监控数据。

- 网络流量（单位：bps 间隔：5分钟，包括出/入流量)

- 包转发率监控 （单位：pps 间隔：5分钟，包括出/入流量)

在监控图表中查看监控数据。

- **监控周期**：监控指标的时间范围，目前分别支持：最近6小时、最近一天、最近两周、最近一个月等。

- **查看监控数据**：将鼠标悬浮于某个图表上，会自动展开图表上的所有监控数据。点击图表上的一个时间点，下方自动展开资源详情信息，可查看具体数据。

![网卡监控](../../../_images/node_monitoring_3.png)

### 节点流量排名

在**节点流量排名**页面，可查看当前物理主机上所有虚拟机的流量排名，支持按如下四项指标进行排序，并支持按关键字进行搜索。

- 出流量 Kbps

- 入流量 Kbps

- 出包流量 PPS

- 入包流量 PPS

![节点流量排名](../../../_images/node_volume.png)

### 虚拟主机

在**虚拟主机**页面，可查看当前计算节点上运行的所有虚拟主机的信息。支持按状态进行过滤和按创建时间、状态更新时间进行排序，并支持按关键字进行搜索。

![虚拟主机](../../../_images/node_host.png)

### 硬盘

在**硬盘**页面，可查看当前计算节点上所有虚机的虚拟硬盘信息。支持按状态进行过滤和按创建时间、状态更新时间进行排序，并支持按关键字进行搜索。

![硬盘](../../../_images/node_disk.png)

### 服务进程

在**服务进程**页面，可查看当前计算节点的所有基础服务进程信息，包括计算服务、告警服务、计算服务、存储服务等，支持按状态和服务角色进行过滤，并支持按关键字进行搜索。

![服务进程](../../../_images/node_service.png)

### 告警记录

在**告警记录**页面，可查看当前计算节点的所有告警信息记录，支持按状态、级别、监控项和告警类型来并支持按关键字进行搜索。可通过告警级别、告警类型和告警时长判断系统异常的影响。

![告警记录](../../../_images/node_alarm.png)

若系统异常恢复完毕后可对该条告警记录添加处理信息，并查看相关日志，点击**处理**，提交处理备注，告警记录的状态将变为`已处理`。

<img src="../../../_images/node_alarm_2.png" alt="处理告警" style="zoom:50%;" />
