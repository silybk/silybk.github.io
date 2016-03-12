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

<b>然后打开你的邮箱你会收到注册确认邮件，点击链接完成注册</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-confirm.png) 

***

### 登录并添加SSH KEYS

<b>进入首页，在左侧找到 Profile Settings</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-profile.png) 

<b>点击进入找到SSH Keys，添加sshkey</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-sshkeys.png) 

***

#### 生成你的ssh key
	
<b>如果你用的是windows，到ftp下载git客户端，安装好打开，输入以下命令</b>

`
ssh-keygen -t rsa -C "xxx@xxx.xx" 
`

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-keygen.png) 


<b>找到你的id_rsa.pub 文件用记事本打开，文件地址上面文字有说明，复制内容到网页上，addkey完成 .</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-addkey.png) 

***

### 测试连通性

<b>输入命令:</b>

`
ssh -T git@domain
`

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-testssh.png) 

***


### clone 项目并建立自己的分支和提交

<b>返回主页，进入项目，复制ssh地址</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-address.png) 

<b>输入git clone address，并进入文件夹</b>

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-clone.png) 

<b>以用户id为test为例，进行如下操作</b>

~~~
git config --global user.name "test"  
git config --global user.email "434464298@qq.com"
git branch test 
git checkout test
git push origin test
~~~

<b>以上命令是进行了设置用户名和邮箱，建立了分支test，切换分支test，并提交到服务器</br>

* example

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-setbranch.png) 

<b> 如果你进行了文件添加和代码修改，并且想提交到服务器时，进行如下操作</b>

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

<b>当你觉得你完成了分配给你的任务，你可以申请merge，简单的说就是把你完成的功能添加到原始项目中，如下申请</b>

![](http://7xr5vo.com1.z0.glb.clouddn.com/myimg%2Fgit-merge.png) 

***

### end

<b>以上就是基本使用，如有问题请先百度，不懂可以联系我 </b>






