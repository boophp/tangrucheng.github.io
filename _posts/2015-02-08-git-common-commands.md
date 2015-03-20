---
layout: post
title: Git常用命令
category: 资源
tags: Git
keywords: Git
description: 
---

## Git独奏

    git --version
    git config -e --system
    git config -e --global
    git config -e
    git config user.name "tang ru cheng"
    git config user.email "tangrucheng@gmail.com"
    git config alias.st status
    git config color.ui true
    git config --unset user.name
    git init demo
    
    git add <file>
    git add -u
    git add -A
    git add .
    git add -i
    git add -f

    git rm
    git mv

    git commit -m "initialized."
    git commit --allow-empty -m "who does commit?"
    git commit --amend --author="tang ru cheng <tangrucheng@gmail.com>"
    git commit --amend --allow-empty --reset-author
    git commit -a

    git reset <commit> [--] <paths> # 不会重置引用，更不会改变工作区，而是用指定状态（<commit>）下的文件（<paths>）替换掉暂存区中的文件
    git reset HEAD <paths> # 相当于取消之前执行的 git add <paths>命令时改变的暂存区
    git reset 或 git reset HEAD # 仅用HEAD指向的目录树替换暂存区中的目录树，工作区不会受到影响，相当于将之前用 git add 命令更新到暂存区的内容撤出暂存区
    git reset [--mixed] <commit> # 改变引用的指向及重置暂存区，但是不改变工作区
    git reset --soft <commit> # 只改变引用的指向，不改变暂存区和工作区
    git reset --hard HEAD # 暂存区和工作区的目录树会被当前工作分支指向的目录树所替换
    git reset --hard master@{2} # 重置master为两次改变之前的值

    git checkout . # 使用暂存区全部的文件替换工作区的文件
    git checkout -- <file> # 使用暂存区指定的文件替换工作区的文件
    git checkout HEAD . # 当前工作分支中的全部文件替换暂存区和工作区中的文件
    git checkout HEAD <file> # 当前工作分支中的指定文件替换暂存区和工作区中的文件
    git checkout <branch> # 更新HEAD以指向branch分支，以及用branch指向的树更新暂存区和工作区
    git checkout <branch> -- <file> # 维持HEAD的指向不变，用branch所指向的提交中的file替换暂存区和工作区中相应的文件，注意会将暂存区和工作区中的file文件直接覆盖
    git rm --cached <file> # 直接从暂存区删除文件，工作区则不做出改变

    git diff # 工作区与暂存区比较
    git diff HEAD # 工作区与当前工作分支比较
    git diff --cached # 暂存区与当前工作分支比较

    git status
    git status -s
    git status --ignored -s
    git log --oneline
    git log --pretty=fuller
    git log --stat # 包含当前提交的状态
    git log --graph # 图表方式显示
    git reflog -1 # reflog是HEAD头指针的变迁记录，而非master分支
    tail -n .git/logs/refs/heads/master
    git reflog show master | head -5

    git branch -v

    git merge <commit>

    git stash # 保存当前的工作进度，会分别对暂存区和工作区的状态进行保存
    git stash save "message..." # 保存工作进度并指定说明
    git stash save --patch # 会显示工作区和HEAD的差异，通过对差异文件的编辑决定在进度中最终要保存的工作区的内容，通过编辑差异文件可以在进度中排除无关内容
    git stash save -k # 在保存进度后不会将暂存区重置，默认会将暂存区和工作区强制重置
    git stash list
    git stash pop # 恢复最新保存的工作进度，并将恢复的工作进度从存储的工作进度列表中清除
    git stash pop <stash> # 从该<stash>中恢复，恢复完毕也将从进度列表中删除<stash>
    git stash pop --index [<stash>] # 除了恢复工作区的文件外，还尝试恢复暂存区
    git stash apply [--index] [<stash>] # 除了不删除恢复的进度之外，其余和 git stash pop 命令一样
    git stash drop [<stash>] # 删除一个存储的进度，默认删除最新的进度
    git stash clear # 删除所有存储的进度
    git stash branch <branchname> <stash> # 基于进度创建分支

    git clean -nd
    git clean -fd

    git tag -m "say bye-bye" old_practice
    git describe

## Tig

配合Tig使用Git会让你更爽 <http://jonas.nitro.dk/tig>

## GitHub

[GitHub秘籍](https://github.com/tiimgreen/github-cheat-sheet)
[Git Subsplit](https://github.com/dflydev/git-subsplit)