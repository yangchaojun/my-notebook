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

## Git忽略规则.gitignore不生效
在项目开发过程中个，一般都会添加 .gitignore 文件，规则很简单，但有时会发现，规则不生效。  
原因是 .gitignore 只能忽略那些原来没有被track的文件，如果某些文件已经被纳入了版本管理中，则修改.gitignore是无效的。  
那么解决方法就是先把本地缓存删除（改变成未track状态），然后再提交。
```git
git rm -r --cached .

git add .

git commit -m 'update .gitignore'
```
