# GiteNote


1.$ git config --global user.name "John Doe"

2.$ git config --global user.email johndoe@example.com

3.$ git help config

4.$ git init   

5.$git add index.html 

6.显示当前目录的路径
pwd  
       
7.删除XX文件
$git rm XX        

8.提交到版本库中 
$git commit -m "add hello world HTML" 

9.$git commit -am “add hello world HTML”  


10.查看提交记录
$git log

11.项目目前的状态
$git status 

12.查看当期分支
$ git branch 

13.创建分支iss53
$ git branch iss53

14.切换到分支iss53
$ git checkout iss53

15.创建分支iss53,并且切换到iss53分支
$ git checkout -b iss53


16.基于origin/dev分支创建本地dev分支，并切换到本地dev分支
$ git checkout  –b dev origin/dev


17.切换分支
$git checkout master
18.合并分支
$git merge hotfix

19.删除分支
$ git branch -d iss52

20.vi+ 文件名   进入文件（不可编辑）
i 进入编辑状态
+命令使用
:q 退出编辑，如果文本内容被修改过，则会报错
:q! 强制退出编辑，如果文本内容被修改过，会丢弃此次的修改
:x 退出编辑并保存


21.用SSH生成公钥和私钥
ssh-keygen -t rsa -C “864805002@qq.com”
把生成的公钥文件用记事本之类的文本编辑软件打开，复制到网站相应的key中
 

22.测试SSH公钥是否成功
ssh git@github.com
tortoiseGit需要在 Putty从新配置，对id_rsa私钥文件进行重新生成



23.克隆远程仓库
$git clone 仓库URL
默认情况下git clone 命令本质上就是自动创建了本地的master 分支用于跟踪远程仓库中的master 分支打开项目文件夹\.git\config文件可以看到master分支和远程仓库master分支的关联
[remote "origin"]
url = https://github.com/Asmewill/GitTest1.git
fetch = +refs/heads/*:refs/remotes/origin/*

[branch "master"]	
remote = origin
merge = refs/heads/master






24.注册远程版本库
$ git remote add origin  https://自己的仓库url地址

25.从远程仓库对应的master分支上拉取代码到本地对应的master分支上update）
$ git pull origin master

26.将本地的master分支推送数据到远程仓库对应的master分支上
$ git push  -u  origin master

27.推送本地仓库的所有分支到远程仓库上去
$ git push -u origin --all
-u 表示参数建立追踪


28.Git会把master分支推送到远程库对应的远程分支上
$ git push origin master


29.Git会把dev分支推送到远程库对应的远程分支上
$ git push origin dev


30.问题 如果本地有个master 和远程的 origin/master分支没有建立跟踪关联需要使用
$ git branch --set-upstream master origin/origin


31.查看本地分支与远程分支的联系
$ git branch –vv


32.查看当前远程仓库信息
$ git branch –r


33.从远程仓库抓取数据到本地
$ git fetch 远程仓库名

34.远程仓库的分支合并
$ git merge 远程仓库名/分支名


35.$ git pull相当于$ git fetch和$git merge远程仓库名/分支名


36.查看远程仓库信息
git remote show [remote-name]

37.远程仓库的重命名
git remote rename 原名 新名字

38.远程仓库的删除(切断本地所有分支与远程仓库的联系)
git remote rm 远程仓库名（origin）

39.二句代码删除远程分支
git branch -r -d origin/branch-name 
git push origin :branch-name   (:不能去掉，代表推送一个空的分支到)




staging area---暂存区
work area---工作区
local repository--本地仓库
remote repository--远程仓库

