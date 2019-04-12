# 序

本书详尽介绍了 .NET 开发人员高效使用 Rx 所需的细节和背景知识，特别是如何在 .NET 中繁多的异步类型与 Rx 可观察对象（Rx observables）间建立联系，以及如何处理错误（errors）、资源分配（resource allocation）和并发（concurrency）问题

一直以来，.NET Framework 都一直在强调异步执行（asynchronous execution）和非阻塞 I/O（nonblocking I/O）的重要性。通过委托（delegates），.NET Framework 始终都在强调高阶函数式编程（higher-order functional programming），通过在委托上自动定义 `BeginInvoke` 和 `EndInvoke` 方法，开发者得以异步调用任何方法（call any method asynchronously）。

但对异步操作（asynchronous operations）来说，BeginInvoke/EndInvoke 模式过于繁琐冗长，需要对代码进行 CPS 变换（continuation-passing style）（译者注：CPS 变换是一种编程风格，用于将内部要执行的逻辑封装到一个闭包内，并将之返回给调用者。通过将控制流程显式暴露给调用者达到控制的目的）。为了改善这一点，基于 .NET 内置的事件（events）与事件处理程序（event handlers），.NET Framework 引入了基于事件的异步模式（event-based asynchronous pattern）。尽管相比于异步委托（asynchronous delegates），基于事件的模式向前跨了一大步，但还有进一步改进的空间。

相对于通过标准 Enumerable/IEnumerator 接口来处理同步流（synchronous streams）的值，LINQ 标准查询运算符（LINQ standard query operators）以更为高级和声明式的形式给出了优雅美观地处理流的答案。如果我们把事件在概念上也当做是一种流的值，就可以通过一种类似的基于 LINQ 的编程模型来处理事件，那岂不美哉？

对事件进行异步调用的另一个弊端是与大多数事件（如鼠标点击事件）不同的是，结合了异步操作的事件只会返回单个值。所以，如果能通过异步方法返回的单个值就能提供类似命令式编程（imperative programming）模型来支持常规控制流条件（regular control-flow-like conditionals）、循环（loops）以及异常处理（exception handling），那岂不美哉？

实践证明，上述两个问题的答案都是肯定的。通过运用某些运算技巧得到的等价关系，我们可以将同步的基于流拉取（synchronous pull-based streams）的 IEnumerable/IEnumerator 接口转换为单体的异步的基于流推送（asynchronous push-based streams）的 IObservable/IObserver 接口。C# 和 VB 中的 async/await 语法让开发人员能够用常规的命令式语法（imperative syntax）编写同步方法和异步方法，LINQ 查询解析（LINQ query comprehensions）则允许开发人员们在同步数据流和异步数据流上进行查询。

这就是 Rx 的初心。那些非 .NET 技术栈的语言都不得不采用「一个/多个 x 同步/异步」这样的组合来做相同的事。使开发人员心情愉悦地高效完成工作的，毫无疑问取决于他们所使用的语言。

如果您是一位清真的 .NET 开发人员，你就一定要保留这本书，并将 Rx.NET 付诸实践！

—— Erik Meijer，“Rx 之父”，[Applied Duality](http://www.applied-duality.com/) 创始人
