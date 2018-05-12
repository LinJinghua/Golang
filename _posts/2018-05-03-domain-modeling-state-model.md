---
layout: post
title: "State Modeling"
description: 领域建模 - 对象状态
image: '/assets/img/blog/taobao-refund.jpg'
category: 'blog'
tags:
- software-system-analysis-and-design
- domain
- modeling
- state
twitter_text: 状态建模
introduction: 领域模型描述了问题域中事物及其之间的关系与量化的约束，我们需要进一步验证模型的有效性与完备性，管理这些事物的生命周期成为有效的方法 - 状态建模。
---

# 状态建模实践

------

## 实践
 1. 使用 UML State Model
    - 建模对象： 参考 Asg_RH 文档， 对 Reservation/Order 对象建模。
    - 建模要求： 参考练习不能提供足够信息帮助你对订单对象建模，请参考现在 定旅馆 的旅游网站，尽可能分析围绕订单发生的各种情况，直到订单通过销售事件（柜台销售）结束订单。

    ![Reservation/Order 对象建模](/assets/img/blog/state-model-reservation.png)

 2. 研究淘宝退货流程活动图，对退货业务对象状态建模

    退货流程参考[Pcbaby百科](https://baike.pcbaby.com.cn/long/22690.html)。
    
    ![淘宝退货流程](/assets/img/blog/state-model-taobao.png)

