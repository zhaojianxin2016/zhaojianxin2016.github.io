---
layout: wp
title: 理解vagrant
---
介绍：<br/>
一款用于快速创建及部署开发环境的工具，一个中间层技术，底层是VirtualBox、VMware等

特点：<br/>
1、便于团队开发环境管理<br/>
2、相同的Vagrantfile文件可以跨平台使用（Linux、unix、Mac OS、windows）

安装：<br/>
1、安装VirtualBox<br/>
  https://www.virtualbox.org/wiki/Downloads <br/>
2、安装Vagrant<br/>
 https://www.vagrantup.com/downloads.html<br/>
3、<a\>如果有现成的virtualfile文件则放到指定路径然后执行 vagrant up<br/>
例：文件在E:\va下  执行如下；<br/>
![插入图片](http://i2.buimg.com/567571/1c98d42b7747b33f.jpg)<br/>
<b\>如果没有现成的文件则执行 vargant init 进行初始化，会生成一个virtualfile文件，之后通过添加box镜像来完成<br/><a>

Boxes：<br/>
vagrant使用一个基础镜像来快速克隆一个虚拟机，这些基础镜像在vagrant中叫做boxes，创建好一个Vagrantfile后需要在当前环境中添加boxes，一般最好先从网上下载相应的box，之后在本地进行添加，添加方法如下：<br/>
1、在本地添加box方法 vagrant box add <name><url><br/>
2、把box文件(例：centos-7.0-x86_64.box)下载后放到当前设定好的目录下，添加一个命为mi_dev的box到环境中<br/>
3、进入到box文件所在指定路径执行 vagrant box add mi_dev centos-7.0-x86_64.box<br/>
4、成功后会有相应的提示信息<br/>

启动和使用SSH登录：<br/>
启动vagrant，命令键入<br/>
vagrant up<br/>

打开virtualbox会看到我们已加载安装的那个box双击进入或点击启动按钮<br/>
vagrant login：vagrant <br/>
Password：vagrant<br/>
默认进来时用户名和密码都是vagrant，这样就完成了vagrant虚拟机的启动，如果默认box界面不好用，可以使用CRT进行连接使用<br/>
ifconfig :查看虚拟机的ip 默认端口22

