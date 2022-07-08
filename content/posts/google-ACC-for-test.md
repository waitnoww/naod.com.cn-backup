---
title: 测试建模：Google ACC
date: 2020-03-06 14:00:50
description: 软件测试教程-测试建模Google ACC。
tags:
- 测试设计
- 测试建模
- 测试相关
- 测试用例
nav:
- 测试设计
categories:
- 测试建模
image: img/blog_img/acc.png
---
ACC（Attributes Components Capability）是Google测试团队使用的一种建模方法，用来快速地建立产品的模型，以指导下一步的测试计划和设计。
在Google内部，ACC得到较普遍的应用，一些工程师还开发了支持ACC模型的Web应用，并将其开源。本文将介绍ACC的内容，所引用的Google+的例子摘录自《How Google Tests Software》一书。此外，本文还将使用启发式测试策略模型（Heuristic Test Strategy Model，简称HTSM）来分析ACC。

运用ACC建模的第一步是确定产品的Attributes（属性）。
---

按照谷歌的定义，Attributes是产品的形容词（adjectives），是与竞争对手相区别的关键特征。按照敏捷开发的观点，Attributes是产品所交付的核心价值（values）。从HTSM的角度，Attributes位于HTSM->Quality Criteria->Operation Criteria，隶属于面向用户的质量标准。

Google+的Attributes如下：

     ○ Social（社交）：鼓励用户去分享信息和他们的状态
    ○ Expressive（表现力）：用户可以运用各种功能去表达自我
    ○ Easy（容易）：让用户以直观的方式做他们想做的事
    ○ Relevant（相关）：只显示用户感兴趣的内容
    ○ Extensible（可扩展）：能够与Google的已有功能、第三方网站和应用（Application）集成
    ○ Private（隐私）：用户数据不会泄漏
ACC以Attribute开始，是产品竞争的自然选择，也符合Google的开发实践。

在Google的项目中，开发人员和测试人员的比例通常是10：1或更高。开发人员会编写大量的自动化测试用例，对产品实施周密的测试，因此测试人员主要关注用户价值和系统级测试。即便如此，测试人员也没有足够的资源测试所有用户行为。所以，测试人员需要通过确定Attributes来明确产品的核心价值，从而区分出测试对象的轻重缓急（priorities）。

获取Attributes的信息源可以是产品经理、市场营销人员、技术布道者、商业宣传材料、产品广告等。测试人员也可以使用“卖点漫游”（The Money Tour）来发掘和检验产品的卖点。

第二步是确定产品的Components（部件）。
---
Components是产品的名词（nouns），可以理解为产品的主要模块、组件、子系统。

从HTSM的角度，Components位于HTSM->Product Elements->Structure和HTSM->Product Elements->Function，即同时具备代码结构和产品功能的特征。

Google+的Components如下：

    ○ Profile（个人资料）：用户的帐户信息和兴趣爱好
    ○ People（人脉）：用户已经连接的好友
    ○ Stream（信息流）：由帖子、评论、通知、照片等组成的有序的信息流
    ○ Circles（圈子）：将好友分组，如把不同的好友归于“朋友”、“同事”等小组
    ○ Notifications（通知）：当用户被帖子提到时，向他显示提示信息
    ○ Hangouts（视频群聊）：视频对话的小组
    ○ Posts（帖子）：用户和好友所发表的信息
    ○ Comments（评论）：对帖子、照片、视频等的评论
    ○ Photos（照片）：用户和好友所上传的照片
Components可以看作功能列表（Function List）的顶层元素，是产品核心功能的清单。

《How Google Tests Software》建议Components列表要尽可能简单，10个Components很好，20个就太多了。其目的是重点考虑对产品、对用户最重要的功能与代码，并避免漫长的Components列表所导致的分析瘫痪。

第三步是确定产品的Capabilities（能力）。
---
Capabilities是产品的动词（verbs），描述了一个Component提供了何种能力来实现一个Attribute。

在HTSM的角度，Capabilities位于HTSM->Product Elements->Function和HTSM->Quality Criteria->Operation Criteria->Capability，刻画了产品实现其核心价值的手段。

Capabilities通常是面向用户的（user-oriented），反映了用户视角的产品行为。测试人员也应该保持Capabilities矩阵的简洁，他们应该关注对用户而言最有价值、最有吸引力的能力，并在合适的抽象层次（right level of abstraction）记录Capabilities。

最重要的是，Capabilities应该是可测的（testable），测试人员能够设计测试来检查产品实现了预期的Capabilities。

有了Capabilities矩阵，测试团队就完成初始的测试计划。这就是前Google测试总监James Whittaker所说的10分钟测试计划（The Ten Minutes Test Plan）。其基本思路是专注于核心属性、核心功能和核心能力，而省略一切不必要的细节。之后，测试团队会利用矩阵去指导测试设计，通常矩阵中的一条Capability就是一个测试对象、测试策略或测试情景，而复杂的Capability会演化出更多的测试设计。

Google所提供的开源Web应用可以分析项目信息，包括测试用例、代码变更、产品缺陷等，以确定Capabilities矩阵中的高风险区域。下图引用自James Whittaker在GTAC 2010的闭幕演讲的幻灯片，是Chrome OS的Capabilities矩阵的热点图（heap map）。图中绿色表示低风险区域，红色表示高风险区域，粉红色和橙色则表示风险居于前两者之间。测试人员可以根据热点图，更好地确定测试优先级，将有限的资源运用在最需要的地方。

许多团队的风险分析依赖于测试人员的经验和猜测，Google的ACC工具则通过分析项目元素（测试用例、代码变更、产品缺陷等）来识别风险。这些被分析的元素位于HTSM->Project Environment，是项目环境的一部分。即便不使用Google的工具，测试人员也可以利用电子表格记录Capabilities矩阵，并自行计算各个条目的风险（一些Google的测试人员也是这么做的）。

在评估风险时，他可以考虑如下因素：

    ● 自动化测试用例：该区域有自动化测试用例吗？测试在定期运行吗？测试通过率是多少？测试用例覆盖了哪些方面，没有覆盖哪些方面？

    ● 手动测试：有人手动测试该区域吗？经过测试，他们对该区域有信心吗？如果满分是10分，他们会打几分？
    ● 代码变更：该区域近期存在代码变更吗？变更频繁吗？变更是新增功能、代码重构、还是缺陷修复？
    ● 代码复杂度：代码的规模是多少？代码是否复杂？如果复杂度的满分是10分，该区域的代码能得几分？
    ● 产品缺陷：该区域的缺陷多吗？有哪些典型缺陷？哪些缺陷已经被修复？哪些缺陷还没有被修复？活跃的缺陷是在快速增加还是稳步下降？
在计算此类风险因素时，测试人员可以采用尽可能简单的度量方法。

一方面，简单的方法更容易解释度量值的含义，从而有助于针对度量值采取相应的行动。  
另一方面，复杂的方法增大了分析的难度，却往往不能提供更多的收益。通过测试去获得直接的反馈，并定期重新度量风险因素，是更注重实效的方法。
