---
title: Git命令
copyright: true
date: 2019-10-17 23:09:34
tags:
---









# 命令大全

## reset

* --mixed：回退到某个版本，只保留源码，回退commit和stage信息

* --soft：回退到某个版本，只回退了commit的信息，不会恢复stage(如果还要提交，直接commit即可)

* --hard：彻底回退到某个版本，本地的源码也会变为上一个版本的内容

* HEAD^^：回退到前N次的提交，是上述的快捷表示



## branch

* [-v]：查看本地分支

* -D[本地分支名]：删除本地的分支
* --remote/-r：查看本地分支追踪的是哪一个远程分支
* -a：查看所有远程分支
* --track newLocalBranch remoteName/remoteBranch：
  * 取回远程主机的更新后，可以在它的基础上，使用gitcheckout命令创建一个新的分支，并使新建的本地分支，追踪指定的远程分支
* --set-upstream master origin/next：手动建立起追踪关系



## log

## diff

## add

* .
  * 添加当前"git status"下显示的除删除文件外的所有修改
* --all：添加所有修改，包括删除文件

## clone

* git clone <版本库的网址> [本地目录名]：
  * 该命令会在本地主机生成一个目录，与远程主机的版本库同名。如果要指定不同的目录名，可以将目录名作为git clone命令的第二个参数
* -o
  * 克隆版本库的时候，所使用的远程主机自动被Git命名为origin。如果想用其他的主机名，需要用git clone命令的-o选项指定
    * $git clone -o jQuery https://github.com/jquery/jquery.git
    * $git remote
    * jQuery

## remote

* 不带选项的时候，git remote命令列出所有远程主机

  * $git remote 
  * origin

* -v

  * 参看远程主机的网址
    * $git remote -v
    * origin git@github.com:jquery/jquery.git(fetch)
    * origin git@github.com:jquery/jquery.git(push)
  * git remote show <主机名>
    * 查看该远程主机的详细信息，一般远程主机名默认命名为origin
  * git remote add <主机名> <网址>
    * 用于添加远程主机
  * git remote rm <主机名>
    * 用于删除远程主机
  * git remote rename <原主机名> <新主机名>
    * 用于重命名远程主机名

  ## fetch

  * gerrit
  * git fetch <远程主机名>  
    * 一旦远程主机的版本库有了更新(Git属于叫做commit)，需要将这些更新取回本地，这时就要用到git fetch命令，通常用来查看其他人的进程，对本地的代码没有影响。默认取回所有分支的更新
  * git fetch <远程主机名>  <分支名>
    * 指定分支名，取回特定分支的更新
    * $git  fetch origin master：取回oringin主机的master分支

  ## pull

  * git pull <远程主机名> <远程分支名>：<本地分支名> 
    * 取回远程主机某个分支的更新，再与本地的指定分支合并
  * git pull <远程主机名> <远程分支名>
    * 如果远程分支是与当前分支合并，则冒号后面的部分可以省略
    * 命令表示取回origin/next分支，再与当前分支合并。实质上，这等同于先做git fetch，再做git merge。
      * $git fetch origin
      * $git merge origin/next
    * git pull origin
      * 如果当前分支与远程分支存在追踪关系，git pull就可以省略远程分支名
    * git pull
      * 如果当前分支只有一个追踪分支，连远程分支名都可以省略
    * git pull -p
      * 如果远程主机删除了某个分支，默认情况下，git pull不会在拉取远程分支的时候，删除对应的本地分支。加上参数-p就会在本地删除远程已经删除的分支
    * --rebase <远程主机名> <远程分支名> : <本地分支名>

  ## push

  * git push <远程主机名> <远程分支名>：<本地分支名> 
    * 