---
title: 测试基础-什么是瀑布模型？
date: 2020-03-26 09:51:36
description: 测试基础理论-什么是瀑布模型？
tags:
- 测试基础
- 测试相关
- 测试理论
- 软件测试
nav:
- 测试基础
categories:
- 测试基础科普
image: img/blog_img/wfm.png
---
## 什么是瀑布模型-例子，优点，缺点和何时使用它


瀑布模型是第一个引入的过程模型。 它也被称为线性顺序生命周期模型。 理解和使用它非常简单。 在瀑布模型中，每个阶段必须在下一阶段开始之前完全完成。 这种类型的软件开发模型基本上用于项目较小且没有不确定的要求。

#### 在每个阶段结束时，将进行一次评审，以确定项目是否走上正轨，以及是否继续或放弃该项目。

             目录
      瀑布模型示意图
      软件工程中瀑布模型的各个阶段
          需求收集和分析
          系统设计
          安装启用
          功能测试
          系统调度
          维护维修
      瀑布模型的例子
      瀑布模型的优点
      瀑布模型的缺点
      何时使用瀑布模型
      瀑布模型与敏捷模型的区别

#### 在此模型中，软件测试仅在开发完成后才开始。 在瀑布模型阶段不重叠。

## 瀑布模型图

![上传成功](https://tva1.sinaimg.cn/large/00831rSTgy1gd73euzzsjj30sk0im3ze.jpg)


## 软件工程中瀑布模型的各个阶段：
瀑布模型有几个阶段。下文对此作了简要说明，并用实例（银行应用程序）来理解瀑布模型。

假设花旗银行正计划开发一个新的银行应用程序

### 需求收集与分析

在此阶段，业务分析师会收集需求，并由团队进行分析。本阶段需求会记录成档。
    
业务分析师根据与客户的讨论记录需求。
    
通过对需求进行分析，会发现项目团队需要回答需求文档中没有提到的以下问题：
- 新的银行应用程序会在多个国家使用吗？
- 我们必须支持多种语言吗？
- 预计有多少用户将使用该应用程序？等
      
### 系统设计

架构师和团队的高级成员致力于项目的软件体系结构、高层和低级设计。
    
确定银行应用程序需要具有冗余备份和故障转移功能，以便随时可以访问系统。
    
架构师创建架构图和高层/低级设计文档。
    
### 实施

开发团队致力于对项目进行编码。
    
他们接受设计文档/工件，并确保他们的解决方案遵循由架构师最后确定的设计。
    
由于应用程序是银行应用程序，而安全性在应用程序需求中是高度优先的，因此它们在应用程序中实现了多个安全检查、审计日志功能。
    
他们还执行其他一些活动，比如高级开发人员检查其他开发人员的代码以解决任何问题。一些开发人员对代码执行静态分析。
    
### 测试

测试小组测试完整的应用程序并确定应用中的任何缺陷。
    
这些缺陷由开发人员修复，测试团队对修复进行测试，以确保缺陷得到修复。
    
他们也进行回归测试看看是否出现了新的缺陷。

该项目同时雇用了具有银行领域知识的测试人员，以便他们能够基于域透视图测试应用程序。
    
安全测试小组被指派来测试银行应用程序的安全性。
    
### 部署

团队在为银行应用程序采购的服务器上构建和安装应用程序。
    
一些高级活动包括在服务器上安装OS、安装安全补丁、加固服务器、安装Web服务器和应用服务器、安装数据库等。
    
他们还与网络和IT管理团队等进行协调，最终在生产服务器上启动和运行应用程序。
    
### 维护

在维护阶段，团队确保应用程序在没有任何停机时间的情况下顺利地在服务器上运行。

运行后报告的问题由团队解决，并由测试小组进行测试。
  
## 瀑布模型实例

在过去，瀑布模型被用于开发企业应用程序，如客户关系管理(CRM)系统、人力资源管理系统(HRMS)、供应链管理系统、库存管理系统、零售链销售点(POS)系统等。

到2000年为止，瀑布模型在软件开发中得到了广泛的应用。即使在敏捷宣言瀑布模型于2001年出版，也一直被许多组织所采用。

近阶段大多数项目都遵循敏捷方法论，某种形式的迭代模型或者其他模型之一取决于它们的项目特定需求。

在过去，瀑布模型开发的应用，如CRM系统、供应链管理系统等，通常需要一年或更长时间才能开发出来。

随着技术的发展，在一些情况下，大型企业系统是在2至3年的时间内开发出来的，但在完成时却是多余的。这有几个原因。

- 当应用程序用C、C+等语言开发时，Java、.NET等新语言(相对地说)将以基于Web的功能取代它们。
    
- 即使应用程序是使用一种新技术开发的，诸如进入市场的竞争对手变得更多、替代品变得更便宜、使用更新技术的功能更好、客户需求的变化等因素增加了开发应用程序的风险。
    
#### 然而，在某些领域，瀑布模式仍然是首选的。

- 考虑一个系统，在这个系统中，人类的生命处于危险之中，系统故障可能导致一个或多个人死亡。
- 在一些国家，这类事故可能导致对负有责任的人实行监禁。
- 考虑一种制度，其中时间和金钱是次要的考虑，人的安全是第一。

#### 在这种情况下，瀑布模型是首选方法。

- 国防部(DOD)、军事和飞机项目的发展遵循了瀑布模式。

- 这是因为必须遵守严格的标准和要求。

- 在这些行业中，需求是众所周知的，而且合同对于项目的交付非常具体。

- 国防部通常认为瀑布模式与它们的收购过程和政府所要求的严格监管程序是兼容的。

#### 话虽如此，像SpaceX等组织使用迭代模型和敏捷方法也正在破坏这些行业。

#### 瀑布模型还用于银行、医疗保健、核设施控制系统、航天飞机等。

### 瀑布模型的优点

- 该模型简单，易于理解和使用。
   
- 由于模型的刚性，这很容易管理-每个阶段都有具体的可交付成果和审查过程。

- 在该模型中，每个阶段只处理和完成一个阶段。阶段不重叠。

- 瀑布模型适用于较小的项目，在这些项目中，需求得到了明确的定义并得到了很好的理解。
    
### 瀑布模型的缺点

- 一旦应用程序在测试在这个阶段，很难回到过去，去改变一些在概念阶段没有得到很好思考的东西。
    
- 在生命周期的后期才会产生任何工作软件。

- 高风险和不确定性。

- 对于复杂和面向对象的项目来说，这不是一个很好的模型。

- 长期和正在进行的项目的不良模式。

- 不适用于需求变化风险中等至高的项目。
    
### 何时使用瀑布模型

- 只有在需求非常清楚、清晰和固定的情况下，才会使用该模型。
    
- 产品定义是稳定的。

- 技术是可以理解的。

- 没有含糊不清的要求。

- 拥有所需专门知识的充足资源是免费提供的。

- 这个项目很短。
    
在瀑布模型中，在产品开发过程中涉及的客户交互非常少。一旦产品准备好，那么只有它可以向最终用户演示。

一旦产品开发完毕，如果出现任何故障，那么修复这些问题的成本就会很高，因为我们需要更新从文档到逻辑的所有内容。

在当今世界，瀑布模型已经被迭代、敏捷等其他模型所取代。

### 瀑布模型与敏捷模型的区别

| 瀑布模型 | 敏捷模型       | 
| -------  |:-------------: |  
| 规划-瀑布模型需要长期规划，这要求需求完全明确 |敏捷项目的规划通常是短期的，因为工作产品是在2到4周内交付的  |
|项目的成功取决于需求的实现|项目成功的基础是向客户交付业务价值|
|瀑布项目是从项目层次结构的顶部驱动的|团队在敏捷项目中是自治的|
|瀑布项目中有许多角色，这些项目还可以有多个层次结构|敏捷项目团队的角色要小得多，例如，Scrum团队只需要三个角色就可以度过难关|
|在需求收集(最初)和测试(最后)期间，与用户进行了大量的通信|在项目期间，与用户进行了稳定的持续通信|
|在开发和其他中间阶段，对最终用户的依赖程度不高|在项目的整个生命周期中，用户都有很大的依赖性|
|完整的需求一开始就有明确的文档记录|需求在项目的生命周期内继续开发，并在需要时(即准时)进行定义|
|不同角色的团队成员有不同的责任级别|平等的责任在角色之间分担|
|严格执行变更控制，并遵循严格的变更控制过程。因此，改变是不被鼓励的，他们对变化的反应也不是很好|敏捷项目是开放的，他们公开接受，并且反应良好|
|像测试这样的质量控制活动是在项目结束时执行的|质量控制活动在整个项目中执行|
|瀑布模型中的过程步骤是严格遵循的，因为该模型更面向过程|敏捷模型更面向人，不太重视过程，可以选择跳过那些价值较低的过程|
|项目在项目结束时交付的特点是发生了大爆炸事件|在项目的每个sprint中都提供工作产品特性|
|在项目的中期，很难衡量项目的进度|项目的进度可以很容易地测量，因为工作特性是经常交付的|
|该项目的进展通常每周与小组一起进行一次审查|在会议期间，每天与小组一起审查项目的进展情况|
