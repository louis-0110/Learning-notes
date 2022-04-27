## global

```js
global.global === global
```

1. setTimeout 返回的是对象不是数字
2. setInterval 返回的是对象不是数字
3. seTImmediate 立即的，类似于setTimeout 0ms
4. console
5. _dirname （当前文件夹名）不是global属性
6. _filename（当前文件名） 不是global属性
7. Buffer (类型化数组，继承自Uint8Array)
8. process
   - kill(pid)  杀死进程 pid：程序进程的id
   - cwd （命令行运行所在路径）
   - exit (强制退出node进程) 0/1
   - argv（获取命令行参数 ， node a b c d）
   -  env 获取环境变量
   -  platfrom （操作系统平台win32 、darwin）

```js
process.kill();
process.cwd();
process.exit();

process.argv;
process.env;
process.platfrom;
```



