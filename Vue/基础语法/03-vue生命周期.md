## 生命周期

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gq92r6l3huj30u023zt9s.jpg" alt="vue生命周期图解" style="zoom:33%;" />

### beforeCreate:

beforeCreate --- 在vue实例完全被创建出来之前(意思就是说vue实例还没有被完全创建出来)被调用，此时数据还没有被初始化，所以无法访问数据

 1. this.$el ----> undefined
 2. this.$data ----> undefined
 3. this.res ---> undefined  // data里面的数据 res

### created:
created --- 在vue实例创建完成后被调用，这个过程已完成了数据的初始化，可以被访问得到，也能获得methods方法；这个过程可以修改数据，这也是渲染之前修改数据的机会。

1. this.$el ---> undefined
2. this.$data ---> {res:'123123'}

### beforeMount:
beforeMount --- 这个过程是在模版已经在内存中编译完成，挂载之前被调用，render函数也是首次被调用，此时完成了虚拟Dom的构建，但并未被渲染，这也是最后一次修改数据的机会。

1. this.$el ---> undefined
2. this.$data ---> {_ob:....,res:'123123'}

### mounted:
mounted --- 这个过程在模版挂载之后被调用，完成渲染，所以我们可以操作Dom。

1. this.$el ---> <div id="app">....</div>
2. this.$data ---> {_ob:...,res:'123123'}
3. this.res ---> '123123'

### beforeUpdate:
这个钩子函数是在重新渲染之前(更新前)调用，这个过程是不能更改数据的；如果在调用这个钩子函数之前数据没有改变的话，是无任何变化的；当数据发生改变之后，此时实例中的数据是最新的，而页面中的数据还是之前旧的，两者并没有达到同步；这个过程会再次调用render函数，它会重新构建虚拟Dom，然后与上次生成的虚拟Dom树利用diff算法进行对比找出差异，为下次的重新渲染做准备。

### updated:
这个过程在重新渲染之后（更新后调用）被调用，已渲染完成，页面更新，此时实例中的数据与页面中的数据是同步的。

### beforeDestroy:
这个过程是vue实例销毁之前被调用，在这个过程中我们可以做一些事情，比如 **清除计时器或事件** 等等。

### destroyed:
vue实例销毁后调用，并且vue实例中**所有的东西都会解绑**，所有的**事件监听器都会被移除**，所有的**子实例也会被销毁**。