git init  # 创建本地仓库
### 初始化信息 用户名 邮箱
```c++
git config --global user.name "XX"
git config --global user.email "853943934@qq.com"
```


### Github 生成秘钥  可以将秘钥给我 我添加你们为可信任设备之后可以自己操作
```
ssh-keygen -t rsa -C XX@XX.com
cat ~/.ssh/id_rsa.pub  
git add .
git commit -m “备注”
git push origin XX远程分支名字 
git branch --set-upstream-to=origin/master  feature/dev
```


### 将本地仓库与github上的远程仓库关联
```
git remote add origin https://github.com/CcTtry/mathcm.git
git remote rm origin
### 建立关联关联之后，查看建立的关联关系
git remote -v
```
### 本地修改了文件之后，
```
### 添加修改的文件到可追踪文件
git add .
### 提交修改的内容
git commit -m”备注信息”
### 将修改的内容推导远程仓库，并覆盖
git push origin master -f
```
### 第二次使用，如何拉取别人更新的代码
```
git remote -v
获取最新代码到本地临时分支(本地当前分支为[branch]，获取的远端的分支为origin/branch])
git fetch origin master:master1  [示例1：在本地建立master1分支，并下载远端的origin/master分支到master1分支中]
git fetch origin dev:dev1[示例1：在本地建立dev1分支，并下载远端的origin/dev分支到dev1分支中]
//查看版本差异
git diff master1 [示例1：查看本地master1分支与当前分支的版本差异]
git diff dev1    [示例2：查看本地dev1分支与当前分支的版本差异]
//合并最新分支到本地分支
git merge master1    [示例1：合并本地分支master1到当前分支]
git merge dev1   [示例2：合并本地分支dev1到当前分支]
//删除本地临时分支
git branch -D master1    [示例1：删除本地分支master1]
git branch -D dev1 [示例1：删除本地分支dev1]
```
