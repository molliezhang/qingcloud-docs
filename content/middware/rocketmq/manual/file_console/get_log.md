---
title: "查看日志及数据文件"
description: 通过 RocketMQ 控制台管理对 Topic 进行管理。
keyword: 云计算,大数据,消息队列,中间件,RocketMQ,Topic
weight: 20
draft: false
---

## 前提条件

- [开启文件管理控制台](../enable)。
- 配置 [VPN](/network/vpc/manual/vpn/)，确保本地可以访问集群网络。即可在本地浏览器里查看日志或下载相应节点的日志文件。

## 获取节点 IP

查看 `Broker`、`Broker-副本`、`名称服务器`、`网页控制台`节点的 `IP`。

<img src="/middware/rocketmq/_images/node_ip.png" alt="获取节点 IP" style="zoom:50%;" />

## 查看文件

1. 在本地浏览器输入 `http://节点 IP`，进入文件查看页面。

   <img src="/middware/rocketmq/_images/file_console.png" alt="文件管理控制台" style="zoom:50%;" />

2. 若开启了密码登录，则还需要输入文件管理控制台用户名和密码。
3. 点击对应路径，即可查看相应的日志文件。

   <img src="/middware/rocketmq/_images/file_console_01.png" alt="查看节点日志" style="zoom:50%;" />
