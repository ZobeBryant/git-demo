# 本demo是测试rebase变基
## 场景
应用的场景有很多，例如
1. 在开发某个版本的sdk时（分支A），紧急插入了一个版本（分支B）。开发人员完成了紧急版需求将B分支合入master分支，此时A的基底需要变为最新的master。
2. 在开发某个版本的sdk时，一些需求（分支C）放入了后续的版本中。后续在分支C上开发完成这些需求后，需要将基底变为最新版本的分支。

## 代码
场景1举例
~~~
git rebase main
// 解决冲突
git add .
git rebase --continue
git push -f

