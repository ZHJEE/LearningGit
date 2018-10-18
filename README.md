# Git与GitHub学习笔记
# Git基础
## 创建版本库

    git init

## 把文件添加到版本库

    gir add <filename>

## 把文件提交到版本库

    git commit -m “message”
-m 后面输入的是本次提交的说明

# 远程仓库
## 使用SSH连接到GitHub

### 检查是否已有SSH keys
在开始生成SSH keys之前你可以检查一下是否已经生成过SSH keys了，如果已经生成过就无需重复。
* 打开Git Bash
* 输入ls -al ~/.ssh检查是否已有SSH keys
* 检查输出列表查看是否有SSH公钥

### 创建SSH KEY
如果你没有SSH keys 那么你就需要生成一个SSH keys。
* 打开Git Bash
* 输入如下命令，使用你自己的邮箱替换youremail@example.com
* 
    ssh-keygen -t rsa -b 4096 -C "youremail@example.com"

本地仓库与远程仓库关联

    git remote add origin git@github.com:cosnux/LearningGit.git

把本地仓库内容推送到远程仓库
    
    git push [remote-name] [branch-name]

例如：

    git push -u origin master

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

