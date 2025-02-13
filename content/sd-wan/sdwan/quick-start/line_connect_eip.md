---
title: "专线经 VPC 访问公网"
linkTitle: "专线经 VPC 访问公网"
keyword: 云计算, 青云, QingCloud,SD-WAN,专线,VPC,公网
description: 本章节介绍专线经 VPC 访问公网。
draft: false
weight: 50
---


本篇指南旨在帮助用户使用光格 SD-WAN 服务实现专线经 VPC 访问公网。 

## 总览

下图展示了本指南所要构建的网络拓扑：

![](../../_images/line_connect_eip_topology.jpg)

    注意：专线经 VPC 访问公网, 请确保专线网段在该区可用的 VPC 网段内, 如下图所示, “北京三区” 可用的 VPC 网段有。

![](../../_images/intranet_router_vpc2.png)

## 操作

第一步：创建 WAN 网。


登录WEB 控制台，在顶部的导航栏里搜索**企业云网**，接着在右边区域点击**创建企业云网**按钮，输入名称即可创建专属 WAN 网。

![](../../_images/create_wan_net.png)

    注意：此步骤只针对首次使用光格 SD-WAN 服务的用户。

第二步：创建专线接入点。


登录WEB 控制台，点击左边导航栏中的**专线**，接着在右边区域点击**创建接入点**，选择**专线**类型并填入相应的信息即可。

![](../../_images/create_wan_line.png)

创建好的专线接入点，状态是审核中。当完成审核、专线链路施工后，用户才可以进行路由配置。目前支持 BGP 和静态路由两种方式。

    注意：对于 BGP 和静态路由两种方式，在配置前请慎重选择，一旦配置不可切换。

第三步：配置专线。


当完成审核、专线链路施工后，用户可以配置专线。本指南以静态路由方式为例，如下所示，指定静态路由即可。

![](../../_images/config_wan_line_route.png) 

    注意：请确保专线网段是该区可用的 VPC 网段。

第四步：创建边界路由器。


WEB 控制台，在顶部的导航栏里搜索**边界路由器**，进入详情页面后，点击**创建**即可创建边界路由器。详细操作可参考[边界路由器操作指南](/network/border_router/manual/border_user_guide)。

第五步：将边界路由器绑定 VPC 网络。


创建 VPC 网络， 点击创建好的边界路由器进入边界路由器详情页，然后点击**绑定 VPC 网络**， 选择创建好的 VPC ，点击 **提交**将内网路由和 VPC 绑定，同时将 VPC 绑定一个公网IP。公网IP的详细文档参考[公网IP](/network/eip)。

![](../../_images/intranet_router_vpc_detail.jpg)

第六步：配置边界路由器的静态路由。


在边界路由器详情页，点击**添加路由**，目标网络指定为默认路由，下一跳是关联的 VPC ，提交配置。

![](../../_images/intranet_router_static_route2.png)

    注意：配置之后需要点击"应用修改"以生效。

完成以上步骤后， 专线可以通过 VPC 绑定的 EIP 访问公网。
