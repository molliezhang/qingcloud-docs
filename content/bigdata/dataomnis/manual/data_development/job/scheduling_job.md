---
title: "配置作业调度"
description: 本小节主要介绍如何配置作业调度。 
keywords: 大数据工作台,数据开发,实时计算,作业,作业调度
weight: 40
collapsible: false
draft: false
---

作业创建完成后，您需要为作业设置调度策略。

## 操作步骤

1. 登录管理控制台。
2. 选择**产品与服务** > **大数据服务** > **大数据工作台**，进入大数据工作台概览页面。
3. 在左侧导航选择**工作空间**，进入工作空间页面。
4. 在目标工作空间选择**数据开发** > **实时计算**，进入实时计算页面。
5. 选择已创建好的作业，点击右侧的**调度设置**，进入调度配置页面。    
   
   在该页面可以查看作业的基础属性，包括**作业名称**、**作业 ID**、**作业描述**。基础属性在调度配置页面均不可修改。

6. 设置调度策略。

   您可以选择[执行一次](#执行一次)或[重复执行](#重复执行)。
   
7. 设置完成后，点击**确定**，完成调度设置操作。

### 执行一次

| <span style="display:inline-block;width:140px">参数</span>  | <span style="display:inline-block;width:520px">参数说明</span>  |
| :------------- | ------------------------------------------------------------ |
| 执行时间 |  可以选择`发布后立即执行`或在`指定时间`执行。            |
| 并发策略 |  支持三种并发策略：允许、禁止、替换。<li>**允许**：允许多个作业实例同时运行。   <li>**禁止**：只允许一个作业实例运行，如果到达调度周期的执行时间点时，上一个作业实例还未运行完成，则放弃本次实例的运行。  <li> **替换**：只允许一个作业实例运行，如果到达调度周期的执行时间点时，上一个作业实例还未运行完成，则终止运行中的实例，启动新的实例。  |
| 超时时间 |  当前作业执行的最大时长，若超时未完成则强制结束作业，作业执行失败。超时时间为 `0` 表示不设置超时时间。       |

<img src="/bigdata/dataomnis/_images/job_run_one.png" alt="执行一次" style="zoom:50%;" />

### 重复执行

| <span style="display:inline-block;width:140px">参数</span>  | <span style="display:inline-block;width:520px">参数说明</span>  |
| :------------- | ------------------------------------------------------------ |
| 生效时间 |  调度将在有效日期内生效并自动调度。生效时间为空表示不限制有效期。            |
| 调度周期 | 支持`分钟`、`小时`、`日`、`周`、`月`、`年`。选择不同的调度周期，还需设置不同的调度参数。  |
| cron 表达式 |  通过字符串的形式表示周期性的计划任务具体执行时间，由设置的调度周期及相关参数自动生成。      |
| 并发策略 |  支持三种并发策略：允许、禁止、替换。<li>**允许**：允许多个作业实例同时运行。   <li>**禁止**：只允许一个作业实例运行，如果到达调度周期的执行时间点时，上一个作业实例还未运行完成，则放弃本次实例的运行。  <li> **替换**：只允许一个作业实例运行，如果到达调度周期的执行时间点时，上一个作业实例还未运行完成，则终止运行中的实例，启动新的实例。  |
| 超时时间 | 当前作业执行的最大时长，若超时未完成则强制结束作业。超时时间为 0 表示不设置超时时间。     |

<img src="/bigdata/dataomnis/_images/job_run_cycle.png" alt="重复执行" style="zoom:60%;" />




