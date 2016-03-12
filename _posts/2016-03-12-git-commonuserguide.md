---
layout:				post
title:				gitlab新手tutorial
header-img:		http://7xr5vo.com1.z0.glb.clouddn.com/bing%2F2016-03-12.jpg-bg
tags:				[git]
categories:			[tutorial]
---
# 新手教程
***

### 注册一个帐号

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-register.png) 

>name:张三<br>
username:zs<br>
email:xxx@xxx.xx<br>
password:***<br>

<p>然后打开你的邮箱你会收到注册确认邮件，点击链接完成注册</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-confirm.png) 

***

### 登录并添加SSH KEYS

<p>进入首页，在左侧找到 Profile Settings</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-profile.png) 

<p>点击进入找到SSH Keys，添加sshkey</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-sshkeys.png) 

***

#### 生成你的ssh key
	
<p>如果你用的是windows，到ftp下载git客户端，安装好打开，输入以下命令</p>

`
ssh-keygen -t rsa -C "xxx@xxx.xx" 
`

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-keygen.png) 


<p>找到你的id_rsa.pub 文件用记事本打开，文件地址上面文字有说明，复制内容到网页上，addkey完成 .</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-addkey.png) 

***

### 测试连通性

<p>输入命令:</p>

`
ssh -T git@domain
`

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-testssh.png) 

***


### clone 项目并建立自己的分支和提交

<p>返回主页，进入项目，复制ssh地址</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-address.png) 

<p>输入git clone address，并进入文件夹</p>

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-clone.png) 

<p>以用户id为test为例，进行如下操作</p>

~~~
git config --global user.name "test"  
git config --global user.email "434464298@qq.com"
git branch test 
git checkout test
git push origin test
~~~

<p>以上命令是进行了设置用户名和邮箱，建立了分支test，切换分支test，并提交到服务器</p>

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-setbranch.png) 

<p> 如果你进行了文件添加和代码修改，并且想提交到服务器时，进行如下操作</p>

~~~
git add .
git commit -m "xxxx"
git push origin test
~~~

* example

你添加了文件readme

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-addreadme.png) 

***

### merge 操作

<p>当你觉得你完成了分配给你的任务，你可以申请merge，简单的说就是把你完成的功能添加到原始项目中，如下申请</p>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-merge.png) 

***

### end








