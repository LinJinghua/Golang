---
layout: post
title: "Use case modeling"
description: 用例建模实践：用例建模、业务建模.
image: '/assets/img/blog/qunar-hotel.png'
category: 'blog'
tags:
- software-system-analysis-and-design
- use-case
- modeling
twitter_text: 用例建模实践.
introduction: 用例建模实践.
---

# 用例建模实践

------

## 1. 用例建模
 - a. 阅读 Asg_RH 文档，绘制用例图。 按 Task1 要求，请使用工具 UMLet，截图格式务必是 png 并控制尺寸
    
    ![Asg_RH Task1 用例图](/assets/img/blog/use-case-Asg_RH-task1.png)
 - b. 选择你熟悉的定旅馆在线服务系统（或移动 APP），如绘制用例图。并满足以下要求：
    - 对比 Asg_RH 用例图，请用色彩标注出创新用例或子用例
    - 尽可能识别外部系统，并用色彩标注新的外部系统和服务
        - 定旅馆在线服务系统：[去哪儿](https://www.qunar.com)。
        - 新用例或子用例色彩：黄色
        - 新的外部系统和服务：蓝色

        ![Asg_RH Task1 用例图](/assets/img/blog/use-case-qunar-reserve-hotel.png)
 - c. 对比两个时代、不同地区产品的用例图，总结在项目早期，发现创新的思路与方法
    - **主功能必须显眼**
    - 细化功能，提供更多选择
 - d. 请使用 SCRUM 方法，在（任务b）用例图基础上，编制某定旅馆开发的需求 （backlog）
    
    | ID | Name | Imp | Est | How to demo | Notes |
    | :---: | :---: | :---: | :---: | :---: | :---: |
    | 1 | 查找酒店 | 50 | 28 | 搜索酒店并展示 | 多种搜索方式(名字、位置)，过滤酒店，排序展示 |
    | 2 | 预订酒店 | 30 | 21 | 选择酒店，生成订单 | 多种订房方式，查看评价，要求登录 |
    | 3 | 管理订单 | 10 | 7 | 增删改查订单 | 要求登录 |
    | 4 | 支付订单 | 10 | 14 | 进行支付 | 要求登录，依赖外部支付系统 |


## 2. 业务建模
 - a. 在（任务b）基础上，用活动图建模找酒店用例。简述利用流程图发现子用例的方法。
    - 活动图

        ![Asg_RH Task1 用例图](/assets/img/blog/activity-qunar-search-hotel.png)
    - 利用流程图发现子用例的方法：从流程图中找出关键步骤(即节点)，往往关键步骤就是一个用例，细化后得到子用例
 - b. 选择你身边的银行 ATM，用活动图描绘取款业务流程

    ![Asg_RH Task1 用例图](/assets/img/blog/activity-atm.png)
 - c. 查找淘宝退货业务官方文档，使用多泳道图，表达客户、淘宝网、淘宝商家服务系统、商家等用户和系统协同完成退货业务的过程。分析客户要完成退货业务，在淘宝网上需要实现哪些系统用例
    - 多泳道图

        ![Asg_RH Task1 用例图](/assets/img/blog/uml-taobao.png)
    - 系统用例
        - 退款申请、仲裁、收退款。


## 3. 用例文本编写
 - 在大作业基础上，分析三种用例文本的优点和缺点

    | 用例文本 | 优点 | 缺点 |
    | :---: | :---: | :---: |
    | 摘要（Brief） | 快捷，不注重细节。适合主成功场景 | 不够详细 |
    | 非正式（Casual） | 覆盖各种场景，编写也比较便捷 | 缺少细节 |
    | 详述（Fully） | 结构化、详尽、无二义的描述 | 耗时长 |
