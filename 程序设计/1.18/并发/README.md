# 并发

并发编程相关概念。

&nbsp;

* **并发**(concurrency)：逻辑上具备同时处理多个任务的能力。
* **并行**(parallesim)：物理上在同一时刻执行多个并发任务。

&nbsp;

需要程序以并发模型设计。执行时依据环境(单核或多核处理器)不同，有不同运行方式和效率。多核处理器真正同时执行多个任务，而单核只能以间隔切换方式运行。所以说，并发是并行的必要条件，并行是并发的理想状态。并行需要多进程(process)或多线程(thread)支持，而并发可在单线程上以协程(coroutine)实现。

&nbsp;

协程通常是指在单线程上，通过协作式切换执行多个任务的并发设计。比如，将IO等待时间，用来执行其他任务。且单线程无竞态条件，可减少或避免使用锁。某些时候，这些用户空间，减少上线文切换的协程比多线程有更高的执行效率。
