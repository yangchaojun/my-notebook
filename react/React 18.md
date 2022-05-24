new concurrent renderer

concurrent feature 

concurrency 并不是一个功能，它是一种机制，这种机制使得React可以为你的UI同时生成多个版本


A key property of Concurrent React is that rendering is interruptible 

可中断的 rendering

实现机制：
1. priority queue 权重队列
2. multiple buffering 多级缓存
