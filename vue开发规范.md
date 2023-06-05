# VUE开发规范

## 编程规范

### 一. 命名规范

#### - 项目命名

全部采用小写，以下划线分割

> 例如：
>
>  mall_management_system

#### -目录规范

全部采用小驼峰，有复数结构时，要采用复数命名法，缩写不用复数

> 例如：
>
> scripts / styles / components / images / utils / layouts / demoStyles / demoScripts / img / doc



【特殊】：vue组件文件及文件夹命名采用大驼峰命名

>例如:
>
>HeadSearch / PageLoading

####  -文件名规范（*JS、TS、CSS*、*LESS*、*HTML*、*PNG*）

全部采用小驼峰

>例如：
>
>renderDom.js / userManagement.html



**tips:命名严谨性**

代码中的命名严禁使用拼音与英文混合的方式，更不允许直接使用中文的方式。 说明：正确的英文拼写和语法可以让阅读者易于理解，避免歧义。即使纯拼音命名方式也要避免采用



### 二. HTML 规范

#### HTML文档类型

统一使用HTML5规范

```html
<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />
    <meta charset="UTF-8" />
    <title>Page title</title>
  </head>
  <body>
    <img src="images/company-logo.png" alt="Company" />
  </body>
</html>
```

#### 缩进

缩进统一使用2个空格

#### 注释

每块功能去都应该使用注释进行功能说明

> 例如：
>
> ```html
> <body>
> <!-- 页面头部 start -->
>   <header>  </header>
> <!-- 页面头部 end -->
> 
> <!-- 页面底部 start --> 
>   <footer></footer>
> <!-- 页面底部 end -->
> </body>
> ```

#### 语义化标签

在项目中尽量使用语义化标签，提升代码可读性

> 例如：
>
> ```HTML
> <header></header>  //页头
> <footer></footer> //页脚
> <main></main> //主题内容
> <section></section> //内容区
> <nav></nav> //导航
> <aside></aside> //附加内容
> <article></artcal> //文章内容
> ```

### 三.CSS规范

#### 选择器命名

类型使用kebab-case命名规范,以中划线链接，ID使用大驼峰命名，命名尽力见名之意

> 例如:
>
> ```css
> .list-wrap{}
> .container{}
> ```

#### 选择器使用

1. 避免直接使用标签选择器
2. 后代相同元素太多，建议使用子选择器
3. 0不需要写单位名

#### less规范

1. 在*styles/var.less*中统一声明全局less变量
2. 避免嵌套层次太多，最多不超过4层

### 四.Javascript规范

#### 命名规范

1. 方法名、参数名、成员变量、局部变量都统一使用小驼峰规范。

2. 方法命名采用动词或者动词➕名词形式
3. 变量命名使用`const`和`let`关键字，不要使用`var`
4. 常量使用全部英文大写加下划线命名 eg:`BASE_URL`



> 例如：
>
> ```js
> const age = 10;
> const BASE_URL = 'www.baidu.com';
> const list = [{name:'小明',age:20}];
> const setCount = (count)=>{}
> 
> let count = 1;
> count = 2;
> ```

**tips:函数方法常用动词:** 见文档最后

#### 字符串

统一使用单引号`''`，不使用双引号`""`

#### 条件循环和循环最多三层

条件判断能使用三目运算符和逻辑运算符解决的，就不要使用条件判断，但是谨记不要写太 

长的三目运算符。如果超过 3 层请抽成函数，并写清楚注释。





## 项目规范

### 一. Vue基础规范

#### 组件使用规范

组件使用两个以上的单词命名，使用PascalCase格式:

1. PascalCase 是合法的 JavaScript 标识符。这使得在 JavaScript 中导入和注册组件都很容易，同时 IDE 也能提供较好的自动补全。
2. `<PascalCase />` 在模板中更明显地表明了这是一个 Vue 组件，而不是原生 HTML 元素。同时也能够将 Vue 组件和自定义元素 (web components) 区分开来。

*tips:* PascalCase 的标签名在 DOM 模板中是不可用的，详情参见 [DOM 模板解析注意事项](https://cn.vuejs.org/guide/essentials/component-basics.html#dom-template-parsing-caveats)。

> 例如：
>
> ```vue
> <scriput>
> 	export default {
>   	name:'TodoItem'
>   }
> </scriput>
> ```
>
> 

3. 基础组件使用base开头，使用完整单词是含义清楚

> ```vue
> components/Base
> |- BaseButton.vue
> |- BaseIcon.vue
> ```
>
> 

4. 和父组件紧密耦合的子组件应该以父组件名作为前缀命名

> ```vue
> components/ 
> |- TodoList.vue 
> |- TodoListItem.vue 
> |- TodoListItemButton.vue 
> |- UserProfileOptions.vue
> ```

####  Prop

- 必须使用 camelCase 驼峰命名 
-  必须指定类型
- 必须加上注释
- 必须加上required 或者default，两者其一

> 例如：
>
> ```vue
> 
> props:{
> 	status:{
> 		type:String,
> 		required:true,
> 	},
> 	title:{
> 		type:String,
> 		default:'这是一个title'
> 	}
> }
> ```



#### 指令

指令都是用缩写语法糖形式

- v-bind: - > `:`
- v-on:  -> `@`
- v-slot: -> `#`



#### v-for

1. v-for必须加上key
2. v-for避免于if在一起使用



#### script结构顺序

 components > props > data > computed > watch > filter > 生命周期函数（钩子函数按其执行顺 

序） > methods



###  二. Router 规范

1. 全部使用懒加载机制
2. name命名规范采用小驼峰规范
3. path采用小驼峰规范
4. 页面传递参数统一使用name

```js

// 传递参数
this.$router.push({name:'userCenter',query:{id:'123'}})
this.$router.push({name:'userCenter',params:{id:'123'}})

// 设置routes

{
  path:'/uploadAttachment',
  name:'uploadAttachment',
  component:() => import('@/views/uploadAttachment/index.vue')
}
```



### 三. 项目目录规范

```
src 源码目录
  |-- api 所有 api 接口 
  |-- assets 静态资源，images, icons, styles 等 
  |-- components 公用组件 
  |-- config 配置信息 
  |-- constants 常量信息，项目所有 Enum, 全局常量等 
  |-- directives 自定义指令 
  |-- filters 过滤器，全局工具 
  |-- datas 模拟数据，临时存放 
  |-- lib 外部引用的插件存放及修改文件 
  |-- mock 模拟接口，临时存放 
  |-- plugins 插件，全局使用 
  |-- router 路由，统一管理 
  |-- store 统一管理 
  |-- themes 自定义样式主题 
  |-- views 视图目录 
    | |-- role role 模块名 
    | |-- |-- role-list.vue role 列表页面 
    | |-- |-- role-add.vue role 新建页面 
    | |-- |-- role-update.vue role 更新页面 
    | |-- |-- index.less role 模块样式 
    | |-- |-- components role 模块通用组件文件夹 
```



#### api目录

1. 文件、变量名与后端保持一致
2. 按照业务模块划分子目录



#### assets目录

> ```
> |assets 
>   |-- icons 
>   |-- images 
>     | |-- background-color.png 
>     | |-- upload-header.png 
>   |-- styles
>   	| |-- common
> ```



### 注释说明

整理必须加注释的地方

- 公众组件的使用说明
- api 目录的接口必须加上注释参数
- store中的state，mutation，action等必须加上注释
- vue文件中的template必须加上注释，模块之间加上 start end注释
- vue文件的methods，每个method 添加注释
- vue文件的date，非常见单词要加注释



#### 其他

1. 尽量不要手动操作DOM
2. 删除无用代码



##### _附录：函数方法常用动词表_

>get 获取/set 设置
>
>add 增加/remove 删除 
>
>create 创建/destory 移除 
>
>start 启动/stop 停止 
>
>open 打开/close 关闭
>
>read 读取/write 写入
>
>load 载入/save 保存
>
>create 创建/destroy 销毁
>
>begin 开始/end 结束
>
>backup 备份/restore 恢复
>
>import 导入/export 导出
>
>split 分割 /merge 合并 
>
>inject 注入/extract 提取, 
>
>attach 附着/detach 脱离 
>
>bind 绑定/separate 分离
>
>view 查看/browse 浏览 
>
>edit 编辑/modify 修改
>
>select 选取/mark 标记 
>
>copy 复制/paste 粘贴
>
>undo 撤销/redo 重做 
>
>insert 插入/delete 移除
>
>add 加入/append 添加
>
>clean 清理/clear 清除
>
>index 索引/sort 排序 
>
>find 查找/search 搜索
>
>increase 增加/decrease 减少 
>
>play 播放/pause 暂停,
>
>launch 启动/run 运行 
>
>compile 编译/execute 执行
>
>debug 调试/trace 跟踪 
>
>observe 观察/listen 监听
>
>build 构建/publish 发布
>
> input 输入/output 输出,
>
>encode 编码 /decode 解码 
>
>encrypt 加密/decrypt 解密
>
>compress 压缩/decompress 解压缩 
>
>pack 打包/unpack 解包
>
>parse 解析/emit 生成 
>
>connect 连接/disconnect 断开
>
>send 发送/receive 接收 
>
>download 下载/upload 上传
>
>refresh 刷新/synchronize 同步
>
> update 更新/revert 复原
>
>lock 锁定/unlock 解锁
>
>check out 签出/check in 签入
>
>submit 提交/commit 交付
>
>push 推/pull 拉 
>
>expand 展开/collapse 折叠
>
> begin 起始/end 结束
>
>start 开始/finish 完成 
>
>enter 进入/exit 退出
>
>abort 放弃/quit 离开 
>
>obsolete 废弃/depreciate 废旧
>
>collect 收集/aggregate 聚集