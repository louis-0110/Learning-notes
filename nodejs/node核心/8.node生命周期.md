## node生命周期

![image-20230208171746283](https://p.ipic.vip/pfryok.png)

timers：存放计时器的回调函数

poll：轮询队列

- 除了timers、checks，绝大部分回调回放入该队列。比如：文件的读取、监听用户请求
- 运作方式：
  - 如果poll中有回调，依次执行回调，直到清空队列
  - 如果poll中没有回调，等待其他队列也没有回调，持续等待，直到出现回调为止

check：setImmediate 队列



> 事件循环中，每次打算执行一个回调之前，必须要先清空```nextTick```队列 和 ```promise```队列