title: 'Hexo + Github , 搭建静态博客'
date: 2015-12-03 15:37:11
tags: [Hexo,github]
categories: Hexo
---
# 环境
##  【安装git】

``` 
$ https://desktop.github.com
```

## 【安转 node.js】

``` bash
http://nodejs.org/download/
```

## 【新建Respository】

``` bash
建立对应仓库，仓库名必须为：【your_github_user_name.github.io】
```

## 【配置github SSH-Key (方便代码提交)】
``` bash
$ cd ~/. ssh 检查本机的ssh密钥

$ ssh-keygen -t rsa -C "youremail.com" 生成新密钥
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):<回车就好>
Enter passphrase (empty for no passphrase):<密钥>
Enter same passphrase again:<密钥>
```

### 【添加SSH-Key到github】
``` bash
$ vim id_rsa.pub 查看密钥，并复制

登陆github系统。点击右上角的 Account Settings—->SSH Public keys —-> add another public keys 添加密钥

$ ssh -T git@github.com
The authenticity of host 'github.com (207.97.227.239)' can't be established.
RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
Are you sure you want to continue connecting (yes/no)?
$ yes
Hi cnfeat! You've successfully authenticated, but GitHub does not provide shell access.
```

### 【设置git用户信息】
``` bash
$ git config --global user.name "cnfeat"//用户名
$ git config --global user.email  "cnfeat@gmail.com"//填写自己的邮箱
```
## 【安装 Hexo】
``` bash
$ npm install -g hexo   //使用git安装hexo

新建Hexo文件夹（ex：D://Hexo）
$ cd D://Hexo

$ hexo init //hexo初始化

$ npm install hexo-deployer-git --save  
```

# 安装 Hexo 主题
``` bash
已iissnan为例
$ git clone https://github.com/iissnan/hexo-theme-next themes/iissnan   //下载iissnan主题
编辑站点文件（ex:D://Hexo/_config.yml)
$ 找到 theme 字段，并将其值更改为 next
```

## 【配置自动部署github文件】
	配置站点配置文件（ex: D://Hexo/_config.yml),找到Deployment节点，type:github（hexo5.0以上为git）,git@github.com:zhchnchn/zhchnchn.github.io.git (冒号后修改为自己的github page 地址)
``` bash
# Deployment
## Docs: http://hexo.io/docs/deployment.html
deploy:
  type: github
  repository: git@github.com:zhchnchn/zhchnchn.github.io.git
  branch: master
```

## 【新建静态BLOG】
``` bash
$ hexo new "My First Blog"
```

## 【启动、生成 Hexo Blog】
``` bash
$ hexo generate  //(hexo g) 生成静态网页
$ hexo start //开启本地调试：http://0.0.0.0:4000
$ hexo generate -deploy //(hexo g -d)生成静态网页并发布到github
```

# 【其它知识链接】
[MarkDown Wiki链接](https://en.wikipedia.org/wiki/Markdown)
[MarkDown 官网](http://www.markdown.cn/)
[NexT 文档](http://theme-next.iissnan.com/)
[Mou 下载](http://25.io/mou/)



