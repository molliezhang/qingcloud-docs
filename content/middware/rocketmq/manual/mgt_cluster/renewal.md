---
title: "续费"
description: 本小节主要介绍如何手动续费 RocketMQ 集群。 
keyword: 云计算,大数据,消息队列,中间件,RocketMQ,手动续费
weight: 60
collapsible: false
draft: false
---

为避免集群到期未续费而造成集群无法使用或其他损失，您可以提前为包年/包月的集群进行续费。

RocketMQ 集群目前支持手动续费和自动续费。

## 前提条件

- 已获取管理控制台登录账号和密码，且已获取集群操作权限。
- RocketMQ 集群计费模式为包年/包月。

## 手动续费

1. 登录管理控制台。
2. 选择**产品与服务** > **消息队列与中间件** > **RocketMQ 服务**，进入 RocketMQ 服务管理页面。
3. 点击目标集群 ID，进入集群详情页面。
4. 在**基本属性**模块，点击集群操作下拉菜单。
5. 展开下拉菜单，点击**手动续费**，弹出手动续费窗口。
   
   <img src="/middware/rocketmq/_images/renewal_manual.png" alt="手动续费" style="zoom:50%;" />

6. 选择续费时长，确认续费价格。
7. 点击**提交**，立即为集群续费。 

## 自动续费

RocketMQ 开启自动续费后，在账户余额充足时，系统将根据设置自动续费。

1. 登录管理控制台。
2. 选择**费用** > **续费管理**，进入续费管理页面。
3. 选择**到期不续费**页签，找到目标集群。

   <img src="/middware/rocketmq/_images/renewal_list.png" alt="续费列表" style="zoom:50%;" />

4. 点击**设置自动续费**，弹出自动续费配置窗口。

   <img src="/middware/rocketmq/_images/renewal_auto.png" alt="自动续费" style="zoom:50%;" />

5. 选择`开启`自动续费，并选择续费时长，确认续费价格。
6. 点击提交，开启集群自动续费。

   在包年包月到期之前，即可自动为集群续费。