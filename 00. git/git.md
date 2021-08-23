# git 基本使用

git config --global user.name "Your name" 绑定用户名

git config --global user.email "emai@example.com" 绑定邮箱

git add readme.text 添加readme文件到缓存区

git add . 添加所有到缓存区

git commit -m "wrote a readme file" 命名并提交

git diff readme.txt 查看文件具体修改了那些内容

git add filename

git add . 添加所有到提交区

git commit -m "first" 提交并命名为first

git log 查看文件版本

git log --pretty=oneline head标题式查看

git reset --hard HEAD^ 回退到上一个版本

cat readme.txt 查看readme文件内容

git reflog 查看命令历史head

git checkout -- readme.text 回到最近一次的git add或者 git commit 之后的状态，也就是撤销最近的修改

git reset head readme.txt 撤销最近的一次git add （然后使用git checkout -- readme.txt就可以回到提交之前写的内容了）

git reset --hard [commit哈希值] (38679ed709fd0a3767b79b93d0fba5bb8dd235f8) 返回到[commit]版本

rm license.txt 删除license.txt文件

## git 连接远程仓库

ssh-keygen -t rsa -C "your_email@example.com" 创建公钥

git remote add origin github.com/Earlcoming/learn-git.git 关联远程仓库并且命名远程仓库名字为origin

git remote set-url jsbasis jsbasis https://github.com/Earlcoming/javascript-basis 删除远程仓库链接

git push -u origin master 提交到远程仓库,第一次提交需要加-u，以后提交到远程仓库只要写git push origin master

git push origin master 除了第一次，以后每一次提交都只要写这个就好了

git checkout -b dev 创建dev分支并且切换到dev分支

git checkout dev 切换分支到dev

git branch dev 创建分支dev

git branch 查看所创建的所有分支,当前分支前面有*

git branch -d dev 删除dev分支

git merge dev 把dev快速合并到当前分支

git log --graph 查看合并图

git merge --no-ff -m "merged bug fix 101" issue-101 --no-ff 不使用Fast forward模式

git remote 查看远程仓库名称

git remote -v 查看所有的远程仓库

git remote rm learn-git 删除远程仓库

git remote rename [old-name] [new-name] 修改远程仓库名称

git branch -r 查看远程分支

git branch -d dev 删除本地分支dev

git branch -D dev 强行删除本地分支

git push origin --delete dev 删除远程分支dev

git push --all origin 推送所有到远程origin分支

## git tag(版本)

打标签

git tag v1.0 给当前分支打标签名为v1.0

git tag 查看标签名

git reset --hard v1.0 回退至v1.0版本

git push origin v1.1 把v1.1版本推送到远程仓库

删除远程版本v1.1(要先删除本地版本1.1)

git tag -d v1.1 删除本地1.1版本标签

git push origin :rsfs/tags/v1.1 删除远程仓库1.1版本标签

## git 别名配置

git config --global alias.co checkout 只要输入git co dev就可以实现git checkout dev

git config --global alias.ci commit git ct -m "name" == git commit -m "name"

git config --global alias.br branch git br == git branch

git config --global alias.st status git st = git status