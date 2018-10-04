# LearningGit
学习git的基本操作

本地仓库与远程仓库关联

    git remote add origin git@github.com:cosnux/LearningGit.git

把本地仓库内容推送到远程仓库

    git push -u origin master

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

