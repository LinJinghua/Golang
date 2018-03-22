---
layout: post
title: "Software Engineering"
description: 系统分析设计第一部分：软件工程部分要点.
image: '/assets/img/blog/The-Mythical-Man-Month.png'
category: 'blog'
tags:
- software-system-analysis-and-design
- software-engineering
- software
twitter_text: 软件工程理解.
introduction: 软件工程理解.
---

# 软件工程部分要点

[TOC]

------

## 简答
 1. 软件工程的定义

    整理自[维基百科:软件工程](https://zh.wikipedia.org/wiki/%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B)
    > 将系统化的、规范的、可度量的方法用于软件的开发、运行和维护的过程，即将工程化应用于软件开发中。或进行研究的学科。

 2. 阅读经典名著“人月神话”等资料，解释 software crisis、COCOMO 模型。

    - software crisis : 即[软件危机](https://zh.wikipedia.org/wiki/%E8%BD%AF%E4%BB%B6%E5%8D%B1%E6%9C%BA)。
        
        人月神话相关原文：
        > 我认为软件困难的部分是在创建规格、设计，并验证其构思，而不是在表达和测试其实现。
        
        概述：
        > 指在软件开发及维护的过程中所遇到的一系列严重问题，这些问题皆可能导致软件产品的寿命缩短、甚至夭折。软件开发是一项高难度、高风险的活动，由于它的高失败率，故有所谓“软件危机”之说。
        
        表现：
        > 1)项目运行超出预算。2)项目运行超过时间。3)软件质量低落。4)软件通常不匹配需求。5)项目无法管理，且代码难以维护。
    
    - COCOMO 模型 : 英文全称为Constructive Cost Model，即[构造性成本模型](https://zh.wikipedia.org/wiki/%E6%9E%84%E9%80%A0%E6%80%A7%E6%88%90%E6%9C%AC%E6%A8%A1%E5%9E%8B)。
        > 通过观察历史项目中工作量和项目规模的数据，通过回归拟合可以得出生产率，工作量，生产率三者间的参数模型，这个参数模型可以用来我们通过软件项目的规模来预测实际的工作量。

 3. 软件生命周期。
    
    软件生命周期(software lifeCycle)也可理解为软件开发过程(software development process)。在软件工程中，软件开发过程是将软件开发工作划分为不同阶段，以改进设计，产品管理和项目管理的过程。大多数现代开发过程可以被模糊地描述为[敏捷(agile)](https://en.wikipedia.org/wiki/Agile_software_development)开发。还有[瀑布(waterfall)](https://en.wikipedia.org/wiki/Waterfall_model)，原型设计，[迭代增量式开发(iterative and incremental development)](https://en.wikipedia.org/wiki/Iterative_and_incremental_development)，螺旋式开发，快速应用程序开发和极限编程等方法。

 4. 按照 SWEBok 的 KA 划分，本课程关注哪些 KA 或 知识领域？

    SWEBok 的 KA 划分见[维基词条](https://en.wikipedia.org/wiki/Software_Engineering_Body_of_Knowledge#SWEBOK_Version_3)，在15个领域中，系统分析与设计课程主要关注软件需求、软件设计、软件构筑、软件配置管理、软件工程管理、软件工程工具与方法。

 5. 解释 CMMI 的五个级别。例如：Level 1 - Initial：无序，自发生产模式。

    整理自[维基词条-CMMI](https://en.wikipedia.org/wiki/Capability_Maturity_Model_Integration)及[百科词条-CMMI](https://baike.baidu.com/item/CMMI#5)。

    ![成熟度级别的特征线](https://upload.wikimedia.org/wikipedia/commons/e/ec/Characteristics_of_Capability_Maturity_Model.svg)
     
     - Level 1 - Initial：无序，自发生产模式。
     - Level 2 - Management：可管理，制定了必要的过程纪律，能重复早先类似应用项目取得的成功经验。
     - Level 3 - Defined：已定义，已将软件管理和工程两方面的过程文档化、标准化，并综合成该组织的标准软件过程。
     - Level 4 - Quantitatively Managed：量化管理，分析对软件过程和产品质量的详细度量数据，对软件过程和产品都有定量的理解与控制。
     - Level 5 - Optimizing：优化管理，过程的量化反馈和先进的新思想、新技术促使过程持续不断改进。


 6. 用自己语言简述 SWEBok 或 CMMI （约200字）

    SWEBOK，英文全称为Software Engineering Body of Knowledge。即软件工程知识体系，由IEEE 计算机协会制作发布。且在2014年2月20日发布了指南第3版。SWEBOK V3一共包括15个知识域，其中包括11个软件工程实践知识域，分别是软件需求、软件设计、软件构造、软件测试、软件维护、软件配置管理、软件工程管理、软件工程过程、软件工程模型和方法、软件质量、软件工程职业实践；以及4个软件工程教育基础知识域——软件工程经济学、计算基础、数学基础和工程基础。后4个是之前版本所没有的。事实上，SWEBOK描述的是广泛共识的知识，随着软件技术的迅速发展，当前一些学术界的研究成果以及产业开始应用的新技术将逐渐普及，SWEBOK V3项目组希望能建立SWEBOK每三年周期性更新的制度，持续改进知识体系。期待SWEBOK能成为持续推进软件工程走向成熟的重要力量之一。
    (参考资料:[解读软件工程知识体系SWEBOK V3
](http://www.360doc.com/content/16/1122/10/31913486_608459924.shtml))


## Personal Software Process(PSP)
 1. 阅读[《现代软件工程》](http://www.cnblogs.com/xinz/archive/2011/11/27/2265425.html)的 PSP: [Personal Software Process 章节](http://www.cnblogs.com/xinz/archive/2011/10/22/2220872.html)。

 2. 按[表格 PSP 2.1](http://www.cnblogs.com/xinz/archive/2011/10/22/2220872.html)， 了解一个软件工程师在接到一个任务之后要做什么，需要哪些技能，解释你打算如何统计每项数据？

 - 工作: 
     - 计划：估计这个任务需要多少时间
     - 开发：需求分析，设计文档，设计复审，代码规范，具体设计，具体编码，代码复审，测试
     - 报告：测试报告，计算工作量，事后总结，改进计划
 
 - 技能: 分析，设计，编程等

 - 统计: 利用git工具记录工作轨迹，利用看板记录重要事件及时间。


## 扩展
 1. COCOMO 模型相关：人月神话的博客-[软件项目计划-估算杂谈](http://blog.sina.com.cn/s/blog_493a845501000aa5.html)：
        
    > COCOMO估算是一种关于软件成本估算的方法，但仅给出一个可行的模型，项目没有足够多的历史数据根本无法确定出各调整因子和系数。但一旦项目建立起这种模型，则通过Cocomo模型得出的项目工作量和项目周期具有更高的准确度。

