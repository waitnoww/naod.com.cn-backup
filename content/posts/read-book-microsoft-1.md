---
title: 《软件测试实践-微软技术专家经验总结》读书笔记-1
date: 2016-10-01 09:37:23
description: 读书笔记分享系列-《软件测试实践-微软技术专家经验总结》读书笔记-1
tags:
- 测试书籍
- 读书笔记
- 测试相关
nav:
- 读书笔记
categories:
- 读书笔记分享系列
image: img/blog_img/book1.png
---
坚持阅读缺陷报告
---
>在项目过程中，测试人员应持续阅读他人或自己提交的缺陷报告，才能更好的理解项目进展，并激发测试灵感和想法
- 了解当前有哪些活跃的缺陷
- 学习测试技巧，完善测试设计
- 获得测试灵感（想法）
- 追踪软件设计
- 总结缺陷模式和类型


测试文档
----
##### 项目所需文档
- 测试计划
- 测试设计规约
- 测试总结报告
- 测试进度报告
- 缺陷报告

##### 其他文档
- 操作文档
- 测试笔记
- 测试资料
- 移交文档
- 测试知识库

##### 测试文档演化
- 测试设计过程
- 测试执行过程
- 测试评估过程
- 测试学习过程

##### 如何实效的设计测试文档
- 它建立了被测试对象的整体模型
- 它提供了可扩展的测试设计框架
- 它提供了测试覆盖的目标
- 它用简洁的形式提供丰富的信息
- 它格式灵活，允许用多种方式记录信息

##### 测试文档维护策略
- 在项目早期，编写测试设计规约，概述测试策略（邀请项目相关人员进行评审）
- 在测试设计规约的指导下，为测试活动收集，复用，编写，改成测试文档
- 将文档集中管理，并周期性地备份
- 请同事评阅文档
- 在项目的重要里程碑完成时，整理已有文档

##### 测试设计规约
- 测试设计规约是一个容器，可以容纳各种测试模型和资料
- 测试人员需要建立测试设计的框架
- 测试想法优于测试用例
- 合理地使用文档模板

##### 测试灵感和测试想法
###### 单个功能
- 该功能与当前测试任务相关吗？
- 该功能存在什么风险？可能会有什么缺陷？
- 通过什么测试可以发现这些缺陷？
- 在上次测试中，该功能表现如何？已有的测试想法，哪些值得再次尝试？哪些不必要再测？
- 依据当前的进度和资源。如何实施这些测试？
- 功能列表是否充分？有没有漏掉一些功能？
###### 组合功能
- 该功能与哪些功能相关？
- 功能的组合有没有揭示出新的风险？可能会有哪些缺陷？
- 哪些功能访问同一批数据？哪些是生产者？哪些是消费者？
- 如何设计测试来同时测试这些功能？
- 如何构造一个有意义的业务流程，让它能够访问尽可能多的功能与数据？
- 对于相互依赖的功能，某个功能的失败是否对其他功能造成恶劣影响？


##### 测试想法的来源
###### 关系人
- 质量标准
- 产品恐惧
- 使用情景
- 领域信息
- 用户
###### 业务
- 目标
- 业务对象
- 产品愿景
- 业务知识
- 法律因素
###### 团队
- 创意想法
- 内部资料
- 你自己
###### 外部
- 标准
- 参考资料
- 搜索
###### 项目
- 项目背景
- 信息对象
- 项目风险
- 测试资料
- 债务
- 交流
- 语境分析
- 交付品
- 工具
###### 产品
- 能力
- 失败模式
- 模型
- 数据
- 白盒
- 产品历史
- 小道信息
- 实际软件
- 技术
- 竞争者

##### 软件质量特性集
- 能力 （完整性 准确性 高效性  可交互性 并发 可扩展性）
- 可靠性
- 可用性
- 魅力
- 安全性
- 性能 （容量  响应度 可达性 反馈 可伸缩性）
- IT能力
- 兼容性
- 可支持性
- 可测性
- 可维护性
- 可移植性