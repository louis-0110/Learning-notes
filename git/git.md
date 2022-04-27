![  ](https://tva1.sinaimg.cn/large/008eGmZEly1gpgok4474kj31az0u0wq8.jpg)

## 5种状态

- 未修改（Origin）
- 已修改（Modified）
- 已暂存（Staged）
- 已提交（Committed）
- 已推送（Pushed）

## 检查修改

1. 已修改，未暂存（检查工作区与暂存区间的差异）

```js
git diff
```

2. 已暂存，未提交（检查暂存区与本地仓库间的差异）

```js
git diff --cached

```



3. 已提交，未推送（检查本地仓库与远程仓库间的修改）

```js
git diff master origin/master

## origin/master 为远程仓库
```



## 撤销修改

1. 已修改，未暂存（撤销工作区的修改）

```js
git reset --hard
```

2. 已暂存，未提交（撤销暂存区的修改）

```js
git reset --hard
```



3. 已提交，未推送（撤销本地仓库的修改）

```js
git reset --hard origin/master

## origin/master 为把远程的代码取回并覆盖
```



4. 已推送（撤销远程仓库的修改）

```js
git reset --hard HEAD^
git push -f

1. 恢复本地仓库
2. 强制推送覆盖远程仓库
```

