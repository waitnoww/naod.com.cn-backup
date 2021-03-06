---
title: 测试用例设计方法-边界值分析
date: 2018-04-12 13:34:41
description: 软件测试教程-如何用边界值分析去设计测试用例
tags:
- 测试设计
- 测试相关
- 测试用例
nav:
- 测试设计
categories:
- 测试用例设计
image: img/blog_img/bjz.png
---
边界值分析（BVA）基于在分区之间的边界处进行测试。这里我们有两个有效边界（在有效分区中）和无效边界（在无效分区中）。

例如，考虑一台打印机，它具有从1到99的副本数量的输入选项。要应用边界值分析，我们将从有效分区中获取最小和最大（边界）值（1和在这种情况下，99分别与在有效分区（在这种情况下为0和100）相邻的每个无效分区中的第一个或最后一个值一起。在这个例子中，我们将有三个等价分区测试（三个分区中的每一个）和四个边界值测试。考虑上一节中描述的等价划分中的银行系统。
什么是边界值分析BVA因为边界值被定义为分区边缘上的那些值，所以我们确定了以下边界值： - $ 0.01（无效边界值，因为它位于无效分区的边缘），$ 0.00，$ 100.00，$ 100.01，$ 999.99和$ 1000.00，所有有效的边界值。因此，通过应用边界值分析，我们将对边界值进行六次测试。

比较我们天真的测试员Robbin所做的事情：他确实达到了一个边界值（100美元），尽管它比设计更偶然。因此，除了仅测试一半分区外，Robbin仅测试了六分之一的边界（因此他在查找任何边界缺陷方面效率较低）。

如果我们考虑所有我们对等效划分和边界值分析的测试，这些技术总共给我们9次测试，而罗比的测试只有16次，所以我们仍然效率更高，效率也高出三倍以上（测试四个分区和六个边界，因此总共10个条件与三个相比）。

通过显示表中的值，我们可以看到没有为7％的利率指定最大值。我们现在想知道帐户余额的最大值是什么，以便我们可以测试该边界。这被称为“开放边界”，因为分区的一侧保持打开，即未定义。但这并不意味着我们可以忽略它，我们仍应该尝试测试它，但问题是如何？

开放边界很难测试，但有不同的方法来处理它们。实际上，问题的最佳解决方案是找出应该指定的边界！一种方法是返回到规范，以查看是否已在其他地方为余额金额说明了最大值。如果是这样，那么我们知道我们的边界值是什么。另一种方法可能是调查系统的其他相关领域。

例如，持有账户余额数字的字段可能只有六位数加上两位小数。这将使最大账户余额为9999999.99美元，因此我们可以将其作为我们的最大边界值。如果我们仍然无法找到关于这个边界应该是什么的任何东西，那么我们可能需要使用直观或基于经验的方法通过输入试图使其失败的各种大值来检查它。

我们可以考虑边界值分析的另一个例子，我们可以将它应用于整个字符串（例如名称或地址）。字符串中的字符数是一个分区，例如，1到30个字符之间是有效边界为1和30的有效分区。无效边界将是0个字符（null，只需按Return键）和31个字符。这两个都应该产生错误消息。