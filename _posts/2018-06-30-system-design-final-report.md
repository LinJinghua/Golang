---
layout: post
title: "Final Report"
description: 系统分析与设计总结报告
image: '/assets/img/blog/commit-dashboard.png'
category: 'blog'
tags:
- software-system-analysis-and-design
- report
twitter_text: 系统分析与设计总结报告
introduction: 系统分析与设计总结报告
---

# 系统分析与设计总结报告

------


 - **项目文档地址：[https://github.com/system-analysis-and-design/dashboard](https://github.com/system-analysis-and-design/dashboard)**
 - **项目代码地址：[https://github.com/system-analysis-and-design/ticket-booking-system](https://github.com/system-analysis-and-design/ticket-booking-system)**


## 课程学习自我总结
 1. 系统学习并实践了软件开发流程，对实际生产开发有了更深了解
 2. 之前选修的《服务计算》课程对应课程后期的微服务架构，这学期加深了了解，学习了架构来源及设计
 3. 领域建模还是一知半解，设计总是与实际情况相悖
 4. 设计能力跟不上需求变化，或者是不能准确把握需求，导致经常重写
 5. 写文档真的比写代码辛苦 (；′⌒`)
 6. 感谢 [LY](https://github.com/linyuy) 支持鼓励我，让我坚持完成任务而不是中途放弃
 7. 但要是问我工作好还是摸鱼好，当然是在工作中摸鱼最好 :P


## PSP 2.1 统计表

| PSP阶段 | 耗时(h) |
| :--: | :--: |
| **计划** | 2 |
| 估计任务耗时 | 2 |
| **开发** | 63 |
| 需求分析 | 5 |
| 生成设计文档 | 10 |
| 设计复审 | 2 |
| 代码规范 | 1 |
| 具体设计 | 10 |
| 具体编码 | 15 |
| 代码复审 | 5 |
| 测试 | 15 |
| **报告** | 2 |
| 测试报告 | 0.5 |
| 计算工作量 | 0.5 |
| 事后总结，提出改进计划 | 1 |
| 总计 | 67 |

## 个人分支的 GIT 统计报告
 - [文档](https://github.com/system-analysis-and-design/dashboard/graphs/contributors?from=2018-03-18&to=2018-06-30&type=c)

    ![用例图](/assets/img/blog/commit-dashboard.png)
 - [代码](https://github.com/system-analysis-and-design/ticket-booking-system/graphs/contributors?from=2018-03-18&to=2018-06-30&type=c)

    ![用例图](/assets/img/blog/commit-ticket-booking-system.png)


## 工作清单
 - RESTful API 设计
    - 每次设计总是与实际应用不服，还要想这动词名词搭配符不符合标准，最后弄得还是四不像，希望以后能改进
 - 文档编写
    - UML 画得是真累，有时候只能摸了
 - 容器编排，docker-compose.yaml文件编写
    - 耗时最长，一直在改错。改完一个以为可以成功了，然后继续对错误改正。而且 docker 建立是真的慢，尽管有缓存，但 build 一次是真的脏，特别是 Vue 和 spring-boot 的依赖包下载，脏


## 博客清单
 - [MongoDB驱动安装](https://linjinghua.github.io/unix-link/)
    - 惨痛选择，还选错了，最终还是用回 MySQL 。 ORM 天下第一
 - [Java 代码优化](https://linjinghua.github.io/java-code-optimization/)
    - 利用 spring-boot 框架开发时得一些思考

