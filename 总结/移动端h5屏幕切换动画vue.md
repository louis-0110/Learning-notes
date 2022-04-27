### vue3

```css
.slide-right-enter-active,
.slide-right-leave-active,
.slide-left-enter-active,
.slide-left-leave-active {
  will-change: transform;
  transition: all 0.5s;
  width: 100%;
  position: absolute;
}

.slide-right-enter-from {
  opacity: 0;
  transform: translate3d(-100%, 0, 0);
}
.slide-right-enter-to {
  opacity: 1;
  transform: translate3d(0, 0, 0);
}
.slide-right-leave-from {
  opacity: 1;
  transform: translate3d(0, 0, 0);
}
.slide-right-leave-to {
  opacity: 0;
  transform: translate3d(100%, 0, 0);
}

.slide-left-enter-from {
  opacity: 0;
  transform: translate3d(100%, 0, 0);
}
.slide-left-enter-to {
  opacity: 1;
  transform: translate3d(0, 0, 0);
}
.slide-left-leave-from {
  opacity: 1;
  transform: translate3d(0, 0, 0);
}
.slide-left-leave-to {
  opacity: 0;
  transform: translate3d(-100%, 0, 0);
}
```

tips:父级最好设置一个position:relative;或 fixed

### vue2

```css
.slide-right-enter-active,
.slide-right-leave-active,
.slide-left-enter-active,
.slide-left-leave-active {
  will-change: transform;
  transition: all 0.5s;
  width: 100%;
  position: absolute;
}
.slide-right-enter {
  opacity: 0;
  transform: translate3d(-100%, 0, 0);
}
.slide-right-leave-active {
  opacity: 0;
  transform: translate3d(100%, 0, 0);
}
.slide-left-enter {
  opacity: 0;
  transform: translate3d(100%, 0, 0);
}
.slide-left-leave-active {
  opacity: 0;
  transform: translate3d(-100%, 0, 0);
}
```

tips:父级最好设置一个position:relative;或 fixed

