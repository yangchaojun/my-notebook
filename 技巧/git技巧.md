[参考连接： ohshitgit](https://ohshitgit.com/zh)

## 修改刚刚commit提交的信息
```git
git commit --amend
```

## 刚刚提交commit就发现还有一个小改动需要添加，但不想新增一个commit
```git
# 继续改动你的文件
git add . # 或者你可以添加指定的文件
git commit --amend --no-edit
# 你这次的改动会被添加进最近一次的 commit 中
# 警告: 千万别对公共的 commit 做这种操作
```
