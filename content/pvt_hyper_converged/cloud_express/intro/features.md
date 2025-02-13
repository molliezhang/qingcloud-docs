---
title: "功能特性"
description: 本小节主要介绍 青立方® 超融合易捷版 产品特性。 
keyword: 青立方® 超融合易捷版产品特性, 功能简介 
weight: 15
collapsible: false
draft: false
---


青立方® 超融合易捷版 (CloudCube Express) 为用户提供了一个具备极致体验的 Web 控制台，以极简的交互界面，让您能够没有任何学习成本快速上手易捷版的核心功能与服务。

## 计算虚拟化服务

青立方® 超融合易捷版的计算虚拟化是整个一体化平台的核心部分，采用裸金属架构的虚拟化技术，通过对物理服务器的计算资源进行抽象，将CPU、存储、I/O 处理能力等物理资源以虚拟资源的方式供用户进行统一的管理、分配使用及调度。以相互隔离的虚拟机的形式构建多个同时在线的环境，实现资源的高效、弹性、动态可配置等能力。

借助绑定网络资源、分布式存储提供的存储资源、SSH 秘钥、防火墙资源、监控告警策略，以虚拟机在线迁移、备份、克隆、镜像模板转换等丰富的功能，可实现更高性价比、更低运营成本、更具灵活性、更加稳定敏捷的业务响应能力。

## 软件定义存储服务

青立方® 超融合易捷版的存储服务采用高性能的企业级分布式共享块存储 QingStor™ NeonSAN。QingStor™ NeonSAN 是由软件定义存储技术实现的新一代分布式超大容量块存储系统（Server SAN），提供 QBD、NVMeoF、iSCSI、QEMU 接口向虚拟化平台提供分布式块存储服务。 NeonSAN 提供企业级的高性能、低延迟与极强的横向扩展能力，在功能、性能、可靠性和易用性等方面兼顾企业核心数据库 OLTP/OLAP、虚拟化等应用的存储需求，可显著降低构建SAN存储平台的总体拥有成本（TCO）。

青立方® 超融合易捷版的存储服务同样借助通用的 x86 服务器架构，与计算虚拟化服务进行融合部署，取代了专有的存储相关设备，减少 FC 网络、HBA 卡等专用配件，减少设备额外能耗及空间的占用。借助 NeonSAN 高效的数据分片技术、数据分布算法、IO 并行处理能力及针对混插模式下的缓存加速优化，配合 SSD、NVMe PCIe 闪存加速卡、RDMA 网卡等硬件，可提供百万级 IOPS 以及高吞吐和微秒级低时延的性能优势。

## 网络虚拟化服务

青立方® 超融合易捷版网络服务能力借助简单易用的基础网络，配合可分配给虚拟机的虚拟网卡实现的。借助虚拟网卡的功能，用户可创建和管理分配给虚拟机的虚拟网卡（包括主网卡和从网卡），支持为虚拟机绑定防火墙、添加标签等功能。

- 基础网络的使用通过 IP 池管理功能实现，用户可将本地环境物理交换机中配置的 VLAN 网段地址添加到 IP 池管理记录中，用于分配具体 IP 地址的网段选择。

- 网络服务提供管理相关功能，如IP使用量、该网段的关联虚拟机资源、多维度（时间区间可选）多粒度（网络流量、包转发率等）的关联虚拟网卡监控及资源使用量监控等。

## 网络安全服务

青立方® 超融合易捷版通过虚拟防火墙机器相关的策略配置规则实现整体网络环境的安全保障。在初次使用时，为用户提供了一个缺省防火墙，为了方便用户使用，缺省防火墙默认仅打开了下行 ICMP 协议和 TCP 22 端口。用户可以借助 “IP/端口集合” 功能把具有相同特征的一组 IP 或者一组端口设置成为 “IP/端口集合”，并且在防火墙规则中进行添加，实现批量管理功能。用户还可以根据当前防火墙规则创建一个备份，用于随时回滚之前的防护墙规则。

## 运维管理服务

### 运维管理总览

平台的概览页提供运维管理总览，将统一直观地展示当前平台的所有资源实时运行状态和资源使用情况。

- 支持查看当前环境虚拟机、硬盘及网络 IP 使用量。

- 支持查看总体环境或单个物理节点的 CPU、物理内存及物理硬盘使用率。

- 提供备份空间占用、集群计算节点运行数量、管理角色服务进程运行情况及基础服务进程的运行状态监控。

- 支持点选查看总体环境或单个物理节点的读写吞吐及 IO 趋势。

- 用户可根据虚拟机的CPU、内存及系统盘资源使用排行获取目前资源使用占比较高的虚拟机，并相应作出配置调整。

- 提供最近一段时间的监控告警及操作日志记录查询。

### 物理资源运维管理

青立方® 超融合易捷版提供了针对物理服务器节点的资源监控、基础服务进程、管理服务进程监控管理、硬件存储资源池管理、物理机-虚拟机-虚拟硬盘资源图形化等多个维度的基础物理资源运维管理。

### 备份管理功能

青立方® 超融合易捷版提供了针对虚拟机及虚拟硬盘两个维度的资源备份及回滚。备份功能用于在块设备级别（block device level）上进行硬盘的备份与恢复，可以同时对多张硬盘做备份（包括系统盘和数据盘），也可以对正在运行的虚拟机做在线备份。

一块虚拟硬盘可以有多个备份链，每条备份链包括一个全量备份点以及多个增量备份点，用户可以随时从任意一个备份点进行虚拟机或虚拟硬盘的资源创建，用于恢复操作。

### 定时任务

定时任务功能可以用来创建一系列定期执行的任务

- 如定时开关机、重启和备份等执行操作。

- 支持主机、硬盘等不同的操作对象。

- 支持在任务的配置过程中还会对有些操作进行相应的限制及配置。
  
   - 如创建备份配置的执行操作可选择添加主机或者硬盘作为操作对对象。
  
   - 备份链长度调整和是否自动删除旧的备份链。

### 通知列表

通知列表功能支持在配置中心中提供的针对监控告警这类功能的使用触发相关的策略时，报警的对象及其方式的设置，默认支持通过邮箱的方式进行发送。

### 监控告警

监控告警功能支持对虚拟机、集群（扩展功能支持）进行监控策略设置以及状态监控，并针对资源的监控属性制定告警规则，在资源状态异常时发出警告。

- 警告会发送至监控对象的详情页监控告警记录中。
- 根据所选的通知列表，默认以邮箱的方式进行告警发送。

### 回收站

回收站功能支持将用户删除的资源，如主机、硬盘、备份、自有镜像等。

- 默认保留两个小时，在这个时间段内用户可以进行恢复操作。两个小后，资源会被彻底进行销毁，不可恢复
- 用户可以主动的在回收站对暂时保留的资源进行手动销毁。

### 用户管理功能

- 用户管理功能承担登录整个环境的用户接入管理的角色。

- 包含对接本地创建的用户及用户既有第三方服务登录用户的接入管理（AD / LDAP）。

- 当使用第三方服务的方式进行接入对接时，需用户输入相关属性信息，之后会自动创建一个与该用户关联的本地用户，便于环境的安全接入登录。

## 扩展服务

### 接入 QingCloud 公有云构建企业混合云

青立方® 超融合易捷版借助内置的光格网络 SD-WAN 服务组件，为企业提供高效的广域网接入能力，扩展和补充现有网络服务能力。通过公有云接入功能，用户可以借助简单的几步配置，分钟级构建本地可控环境到 QingCloud 公有云之间的专属网络，实现网络层打通，以更低成本获得高品质的网络连接与云端资源环境的访问体验。

借助青立方® 超融合易捷版及其公有云接入能力，用户可以在节省自建设备投资、人员投入、快速低成本构建与公有云端的无缝连接，推动实现用户的混合云架构就绪环境，助力用户低门槛一步全面触云。

### 一键选装 QingCloud 桌面云功能服务

QingCloud 桌面云是基于 QingCloud IaaS 平台研发的新一代企业级办公解决方案，可基于 QingCloud 的 IaaS 平台独立部署。每个桌面云用户基于瘦客户机连接自己的办公桌面，与传统办公使用的 PC 机相比，桌面云有集中管控、轻量级运维、数据安全等诸多优势。

青立方® 超融合易捷版默认包含可选的桌面云功能服务组件，通过便捷部署的方式，无需购买具体的并发连接用户授权即可获得云桌面服务的能力。桌面云将通过调用的方式使用QingCloud 企业级云平台 Express 版本提供的计算、存储、网络、安全等资源，同时支持以桌面为中心、用户与资源权限策略控制为辅的独立管理控制台界面。

### V2V 迁移

V2V 迁移工具提供静态迁移能力，可将其它云平台（vmware、Xen）等的虚拟主机系统及数据通过 WEB 上传的方式拷贝到当前平台目的主机。
