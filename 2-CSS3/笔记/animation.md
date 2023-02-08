## animation

animation: <name> <duration> <timing-function> <delay> <iteration-count> <direction> <fill-mode>;

- name:运动动画名字 用@keyframes 定义 0% 到 100% 或 from 到 to

```css
@keyframes name{
  0%{
    width:100px;
  }
  100%{
    width:300px;
  }
}
@keyframes name{
  from{
    
  }
  to{
    
  }
}
```

- duration 运动时长 s / ms

```css
div{
  animation: name 5s; 
  animation: name 5000ms;
}
```

- timing-function 运动过程状态 贝塞尔曲线 / steps函数

- delay 动画延迟时间 执行

- iteration-count 动画循环/重复次数

- direction 方向/动画执行方向 从0 到 100，还是从100到0 

  * normal：正常方向

  * reverse：反方向运行

  * alternate：动画先正常运行再反方向运行，并持续交替运行

  * alternate-reverse：动画先反运行再正方向运行，并持续交替运行

- fill-mode 设置运动之外的状态

  - none：默认值。不设置对象动画之外的状态

  - forwards：设置对象状态为动画结束时的状态

  - backwards：设置对象状态为动画开始时的状态

  - both：设置对象状态为动画结束或开始的状态

    
> both 开始时对象状态是动画第一帧的状态，结束时对象状态是动画最后一帧的状态

```css
@keyframes jumps {
  0% {
    transform: translate(0)
  }

  10% {
    transform: translateY(5px) scaleX(1.2) scaleY(.8)
  }

  30% {
    transform: translateY(-13px) scaleX(1) scaleY(1) rotate(5deg)
  }

  50% {
    transform: translateY(0) scale(1) rotate(0)
  }

  55% {
    transform: translateY(0) scaleX(1.1) scaleY(.9) rotate(0)
  }

  70% {
    transform: translateY(-4px) scaleX(1) scaleY(1) rotate(-2deg)
  }

  80% {
    transform: translateY(0) scaleX(1) scaleY(1) rotate(0)
  }

  85% {
    transform: translateY(0) scaleX(1.05) scaleY(.95) rotate(0)
  }

  to {
    transform: translateY(0) scaleX(1) scaleY(1)
  }
}
