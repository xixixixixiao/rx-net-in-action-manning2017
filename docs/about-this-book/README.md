# 关于本书

_Rx.NET in Action_ 为开发人员提供了完整的 Reaction Extensions 指南。本书包含有理论讲解、最佳实践和使用技巧，让你在开发中充分领略 Rx 之美。

## 谁需要这本书

_Rx.NET in Action_ 适用于需要编写这类应用程序的 .NET 开发人员：基于事件（event-based）和异步（asynchronous）、需要在事件和基于推送（push-based）的源上提供较强处理与查询能力等。

本书同样适用于对反应式编程（reactive programming）和 Rx 技术感兴趣、但暂时不会使用这门技术的开发人员。将 Rx 技术加入到你的技术栈内对你未来的项目非常有用，反应式编程是一个热门话题，这种热门还将持续很久。

本书主要是用 .NET 版本的 Rx，代码示例使用 C# 语言，熟悉 C# 的读者会觉得宾至如归。

本书适用于所有 .NET 支持的平台（包括 .NET Core）。

## 本书结构

本书计有两大部分，列 11 章。

第一部分介绍反应式编程和必须的 .NET 技能，以便能掌握 Rx 的功能使用。

- **第 1 章** 探讨反应式编程范式，介绍反应式宣言（Reactive Manifesto）。该章节介绍使用 Rx 并解释为何使用、何时使用 Rx 的问题
- **第 2 章** 初次接触 Rx，并一步步引导如何使用 Rx。该章节提供有一个简单的例子，该例将展示引入 Rx 前后应用程序的不同
- **第 3 章** 概述 Rx 使用的函数式编程（functional programming）理论和技术，并介绍它们如何在 .NET Framework 和 C# 语言中实现的。

第二部分深入探究 Rx 的更多细节，从创建可观察对象（observables）和观察者（observers），到控制其生命周期（lifetimes）以及对在其上创建的查询的反应。

- **第 4 章** 介绍创建可观察序列（observable sequences）的方法，并展示如何通过 enumerables 和内建（built-in）创建运算符（creation operators）创建同步可观察对象（synchronous observables）
- **第 5 章** 介绍 Rx 处理异步代码的方法，以及如何将原生 .NET 异步类型（native .NET asynchronous types）桥接（bridge）到可观察对象。该章节还将讨论异步代码在现代应用程序中的重要性，以及如何在应用程序中加入定时行为（periodic behavior）。
- **第 6 章** 讨论可观察对象和观察者的关系（observable-observer relationship）以及如何控制它。该章节将介绍多种场景下创建观察者的最佳方法，以及如何限制观察者订阅（subscription）的生命周期。
- **第 7 章** 探讨冷热可观察对象的区别，介绍 Rx subject。该章节介绍如何在为观察者订阅可观察对象时控制该可观察对象的状态，以及如何在观察者之间共享结果
- **第 8 章** 介绍 Rx 中的基本查询运算符。Rx 通常被称作 LINQ to Events，了解 Rx 运算符的细节有助于构建功能强大的查询，从而节省开发者的时间和精力
- **第 9 章** 接着第 8 章的内容，讲解可观察对象的分区和组合等高级方法。该章节将介绍如何通过条件对元素进行分组，以及如何对相关可观察对象做出反应
- **第 10 章** 深入探讨 Rx 并发模型（concurrency model）和同步（synchronization）。该章节将介绍调度器（schedulers）概念、Rx 所提供的的调度器，以及介绍如何控制 Rx 查询的时间和运算位置。
- **第 11 章** 探讨 Rx 查询如何免受错误的影响，并对查询处理（query processing）过程中可能发生的错误做出反应。该章节还涵盖了如何管理可观察对象和 Rx 查询所使用的资源

本书还有三个附录：

- **附录一** 总结 .NET 异步编程概念
- **附录二** 介绍 Rx Disposables 及其使用方法
- **附录三** 介绍如何测试 Rx 运算符和查询

本书旨在用作指南和参考。如果你是新手，我建议你从头阅读。如果你已熟悉 Rx 的概念，则可根据实际情况翻阅特定章节。

## 关于代码

本书包含大量示例代码，代码以等宽字体印刷，以区别于普通文本。有时代码会加粗，用来表示相关代码已发生变更，比如在现有代码中添加新功能。

本书多处源码在印刷时进行了重新排版，通过添加换行符、重写缩进等以适应图书纸张的可用空间。还有少数几处会更加极端，不得不使用特殊的换行符号（<img src =“img / enter.jpg”/ />）。此外，在文本中使用的代码会把源码中的注释移除，这些注释用于突出重点。

本书源码可在出版社网站（[www.manning.com/books/rx-dot-net-in-action](http://www.manning.com/books/rx-dot-net-in-action)）和 GitHub（[https://github.com/tamirdresher/RxInAction](https://github.com/tamirdresher/RxInAction)）下载。GitHub 仓库（repository）的 README 文件给出了源码使用的说明。

本书电子版会为列表和代码片段进行代码着色。蓝色（blue）用于基础类型（primitive types）和关键字（keywords），水色（aqua）用于突出用户定义的类型，红色（red）用于字符串文字，棕色（brown）用于字符串参数占位符，绿色（green）用于注释，黑色（black）为用户代码。

## 作者在线社区

当你购买本书时，你同时获得了免费访问由 Man 宁 出版社提供的私有在线社区的权限，你可以在该社区内对本书进行评论、提出技术问题，并从作者和其他用户那里获得帮助。你可以通过 www.manning.com/books/rx-dot-net-in-action 访问社区或订阅社区。该页面同时还提供了有关诸如「如何在注册后访问社区」、「实用帮助」和「社区规定」等信息。

Manning 出版社对读者的承诺是提供一个让读者可以与作者和其他读者进行沟通的平台，但这并不是绝对的，作者和读者在在线社区的贡献都是他们自愿且无偿的。我们建议你提出一些有挑战性的问题来吸引大家的注意。一旦本书出版，你就可以在出版社的站点上浏览作者的在线版块以及历史存档。

曼宁对读者的承诺是提供一个场所，让读者之间以及读者与作者之间进行有意义的对话。 这并不是对作者任何具体参与

## 其它线上资源

如你对 Rx 很感兴趣，你可以访问 Rx 门户站点 http://reactivex.io，它提供有 Rx 开发者中心，包含了 Rx 库和这一领域的其它最新资讯。

Rx.NET 是一个开源项目，可以在 https://github.com/Reactive-Extensions/Rx.NET 查阅完整代码额讨论。

如果你有就 Rx 提问，可以访问我们的 gitter 频道（https://gitter.im/Reactive-Extensions/Rx.NET）或者 slack 的 #rx 频道（需要在 .NET Core Slack 频道 http://tattoocoder.com/aspnet-slack-sign-up/ 进行注册）。
