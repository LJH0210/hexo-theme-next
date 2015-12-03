title: Git 常用命令
date: 2015-12-03 22:24:07
tags: github
categories: github
---


好记性不如烂笔头，既然玩了玩Hexo+GitHub，那么就将这2天学到的一点点东西整理出来，也好帮助自己理解Git是个啥玩意（啥玩意？人美活好的妹子~哈哈~··），更详细官方文档请查看[Git 中文文档](http://git-scm.com/book/zh/v2);

# 创建仓库

复制一个已存在的仓库

```
$ git clone (giturl)
```

新建本地仓库
	
```
$ git init (本地仓库目录下)
```

# 修改
显示工作路径下已修改文件

```
$ git status
```

对比本地仓库和中央仓库代码文件

```
$ git diff
```

标记需要commit的文件

```
$ git add   //标记所以已修改文件
$ git add -p <file> //标记file文件
```

commit
```
$ git commit -m <message> //提交已标记文件
$ git commit -a  -m <message> //提交所有已修改文件
```

将本地仓库push到远程仓库

```
$ git push
```

#分支标签

列出所有分支标签

```
$ git branch
$ git tag
```

基于当前分支创建分支、标签

```
$ git branch <new-branch>
$ git tag <new-tag>
```

切换分支标签

```
$ git checkout <branch/tag>
```

删除本地分支、标签

```
$ git branch -d <branch>
$ git tag -d <tag>
```


同步远程仓库

```
$git pull
```

合并指定分支到当前分支

```
$ git merge <branch>
```

衍合指定分支到当前分支

```
$ git rebase <branch>
```

# 远程操作

查看远程版本库信息

```
$ git remote -v
```

添加远程版本库

```
$ git remote add <remote> <url>
```

从指定远程版本库获取代码

```
$ git fetch <remote>
```

从指定远程库下载代码及快速合并

```
$ git pull <remote> <branch>
```

提交至指定远程库

```
$ git push <remote> <branch>
```










