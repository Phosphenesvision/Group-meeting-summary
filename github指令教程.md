

```
cd github1/
git clone https://github.com/Phosphenesvision/Reading_Notes_about_DL.git
```

好像还有另外一种ssh的传输协议，等我有空了搞搞这个东西，下面介绍一些命令的作用

```
cd Reading_Notes_about_DL/    ###进入某个project的文件
git pull   ###拉下来，保持与云端同步
git branch   ###查看在哪个分支下面
git checkout -b zzp origin/zzp	###第一次去其他分支
git checkout zzp	###去其他分支
然后在相应的分支下做修改
git add Spatial\ As\ Deep\:\ Spatial\ CNN\ for\ Traffic\ Scene\ Understanding.pdf	###添加文件，如果是删除文件后面也要加名字
git add .	###只修改不上传新的东西
git commit -m "上传一篇有关于SCNN的论文"	###对这个操作作出一点解释
git status	###查看现在的状态
git push origin master	###把本地修改提交到master分支上，输入用户名密码
git push	###同上
```

本来想协议下ssh传输的教程，结果呵呵，发现官网上给的教程很全，行吧，去官网上查看就行了，在右上角头像那里，点进setting去就ok了

# 第一步，建立文件夹，下载github

1.当场演示如何创建一个项目，每创建一个项目就是一个仓库，repository

2.本地创建文件夹

3.http协议传输内容

4.ssh协议传输内容，相关配置按照官方指令来

# 第二步，独自一人完成项目的本地基础操作

```
cd Reading_Notes_about_DL/    ###进入某个project的文件
git pull   ###拉下来，保持与云端同步
git add Spatial\ As\ Deep\:\ Spatial\ CNN\ for\ Traffic\ Scene\ Understanding.pdf	###添加文件，如果是删除文件后面也要加名字
git add .	###简便的方式
git commit -m "上传一篇有关于SCNN的论文"	###对这个操作作出一点解释
git status	###查看现在的状态
git push	###同上
```

关于git add这个指令，有很多形式，可以参考<https://juejin.im/post/5c2ecd3e6fb9a049ef26b6c4>

# 第三步，多人以参与者身份合作项目

1.了解分支的概念，branch

2.如何创建这个项目

指路<https://segmentfault.com/a/1190000015798490>

创建项目 拉到本地 创建新的分支 邀请参与者

3.如何参与这个项目

```
checkout -b zzp origin/zzp	###第一次去其他分支
git checkout zzp	###第二次去其他分支
然后在相应的分支下做修改
git add .	###更改全部
git commit -m"555555555555"
git push origin zzp ###把分支更改push到远方仓库
git checkout master
git merge --no-ff -m"写合并分支的commit" Bob ###切换到master并且合并分支至master不删除bob分支
git push origin master ###主分支更改push到远方仓库
```

# 第四步，fork参与项目

教程指路<https://blog.csdn.net/yxys01/article/details/78316649>

1.fork

并用下面指令保持同步

```
git clone git@github.com:Phosphenesvision/Self-Driving.git
git remote add upstream https://github.com/wsustcid/Self-Driving.git
git remote -v
```

2.本地修改远程上传