---
layout: post
title: "Software Architecture"
description: 架构建模 - 云时代的架构实践
image: 'https://facebook.github.io/flux/img/flux-simple-f8-diagram-explained-1300w.png'
category: 'blog'
tags:
- software-system-analysis-and-design
- architecture
- modeling
twitter_text: architecture & cloud service
introduction: An architecture is the set of significant decisions about the organization of a software system, which describe the selection of the structural elements and their interfaces by which the system is composed, and their behavior as specified in the collaborations among those elements
---

# 架构建模 - 云时代的架构实践

------

## 实践

 - 描述软件架构与框架之间的区别与联系
    - 定义
        > 软件架构就是把系统分解为一些部件，描述这些部件的职责及它们之间的协作行为。
        > 框架是特定语言和技术的架构应用解决方案。
    - 区别
        1. 软件架构注重决策，软件框架注重实现
            > Architecture is About Intent, not Frameworks - [Robert C. Martin (Uncle Bob)](https://sites.google.com/site/unclebobconsultingllc/)
        2. 在软件开发流程中，软件架构对应设计阶段，软件框架对应编码实现阶段
    - 联系
        1. 共性：两者都为软件开发提供了指导方案。
        2. 连续性：软件架构位于软件框架上层，软件框架往往是软件架构的编码实现。

 - 以你的项目为案例
    - 绘制三层架构模型图，细致到分区
        ![用例图](/assets/img/blog/architecture-movie.png)
    - 结合你程序的结构，从程序员角度说明三层架构给开发者带来的便利
        1. 降低开发复杂度。因为三层架构把大系统细分成耦合度很低的小模块，方便理解及编程
        2. 加快开发速度。同上， 由于模块间耦合度很低，可以实现并行开发
        3. 降低维护成本。同上， 模块功能单一且模块间耦合度低，易于扩展及维护

 - 研究 VUE 与 Flux 状态管理的异同
     - 相同
        1. 目的都是解耦，降低开发复杂度
        2. 都脱胎于 MVC 思想
        3. VUE 中专门提供状态管理工具的 Vuex 类似于 React(Flux 的一种实现) 里面的 Redux 的状态管理器，用来管理 Vue 的所有组件状态
    - 区别
        1. 实现不同：VUE 是双向数据流(劫持数据属性)，Flux 是单向数据流(类发布订阅)
        2. 性质不同：Flux 是一种前端状态管理架构思想，VUE 是基于 Flux 的设计思想的一种前端状态管理框架

