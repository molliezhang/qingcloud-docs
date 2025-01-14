---
title: "调整节点数量"
description: 介绍如何新增及删除 QKE 集群节点。
draft: false
enableToc: false
keyword: 青云, QingCloud, 云计算, QKE, 横向扩容, 伸缩, 节点
weight: 10
---

QKE 集群支持通过新增或删除节点来进行集群横向扩缩容。

> **说明**
>
> 您也可以通过**自动伸缩**功能来自动调整节点数量。具体操作请参见[节点自动伸缩](../auto_node/)。

## 增加节点

您可以通过新增节点来应对应用逐步增多带来的压力。

1. 登录 QingCloud 管理控制台。

2. 在控制台顶部的导航菜单中，选择**产品与服务** > **容器服务** > **容器引擎 QKE**，进入 QKE 集群列表页面。

3. 点击目标集群 **ID** 号，进入集群详情页面。

4. 在页面右侧的**节点**页签，点击**新增节点**。

   ![](../../../_images/add_node.png)

5. 选择新增节点类型，并配置节点信息：节点名称、数量、IP、CPU、内存等。

   建议新增节点类型与集群主节点类型一致。

   > **说明**
   >
   > - 建议新增节点类型与集群主节点类型一致。
   > - 基础型节点及客户端节点进支持设置节点名称、数量及 IP，不支持设置 CPU、CPU 体系架构、内存及硬盘大小。
   > - `QKE v1.0.1` 以及更老的版本只支持同一种类型的工作节点，如果之前是性能型节点，那么之后也只能增加性能型节点，如果增加了其他类型的节点，可能会导致需要挂载硬盘的工作负载无法启动。

6. 点击**提交**。

## 删除节点

当集群服务能力过剩时，您也可以删除多余的节点，以节省资源和费用。

> **注意**
>
> - 删除前请确保KE 集群内有足够资源容纳迁移的 Pod。
> - 删除节点不可恢复，请谨慎操作。

1. 登录 QingCloud 管理控制台。

2. 在控制台顶部的导航菜单中，选择**产品与服务** > **容器服务** > **容器引擎 QKE**，进入 QKE 集群列表页面。

3. 点击目标集群 **ID** 号，进入集群详情页面。

4. 在页面右侧的**节点**页签，勾选需要删除的节点，点击**删除**，弹出提示框。

   ![](../../../_images/delete_node.png)

5. 确认无误后，点击**确认**。

