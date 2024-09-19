+++
author = "若水"
title = "Git 常用命令"
date = "2024-06-18"
description = "Git 使用"
categories = [
    "Tools"
]
tags = [
    "工具",
]
+++

# 一、Git常用命令
- git clone [url]: 克隆一个远程仓库到本地。
- git add [file]: 将文件添加到暂存区。
- git commit -m "[message]": 将暂存区的文件提交到本地仓库，并附带提交信息。
- git diff: 显示工作目录和暂存区文件的差异。
- git branch: 列出本地分支。
- git checkout [branch/tag/commit]: 切换到指定分支、标签或提交。
  ... git checkout -b 分支名
  ... git checkout tags/v1.0
- git merge [branch]: 将指定分支合并到当前分支。
- git pull: 拉取远程仓库的更新并合并到本地仓库。
  ... 比如 git pull origin
- git push: 将本地仓库的更新推送到远程仓库。
  ... 比如 git push origin branch-v3.25.0
- git revert [commit]: 撤销指定提交的修改，并创建一个新的提交
- git remote -v 查看远端地址
- git remote set-url origin https://gitee.com/xx/xx.git (新地址)
- git remote add [url] 添加远程仓库
- git branch <new-branch-name> <tag-name> 会根据tag创建新的分支.
- git branch 查看本地分支
- git branch -r 查看远程分支
- git ls-remote --tags origin 查看远程tag
- git tag 查看本地
- git submodule  add  <sub_git_url>  相对路径 ： 用来添加子模块

# 二、案例：github fork 别人代码，然后基于某个tag 建分支
  1. 添加源：git remote add upstream https://github.com/qicosmos/ormpp.git
  2. clone fork后的仓库 
  3. git fetch upstream  同步源
  4. 查看tag 
  5. git branch <new-branch-name> <tag-name> 创建分支
  6. git push origin <new-branch-name>


# 三、案例：Git 关联 GitHub
## 打开Git Bash,设置用户信息
    git config --global user.name "名字"
    git config --global user.email "邮箱"
## 查看已配置的信息
    git config --global user.name
    git config --global user.email

# github fork 别人代码，然后基于某个trunk建分支
### lvgl 项目为例
1. fork 别人的仓库到自己的github
2. git clone https://github.com/simazhuge/lvgl.git
3. git remote add upstream https://github.com/lvgl/lvgl.git
4. git remote -v
5. git fetch upstream
6. git switch -c   upstream/release/v9.2
7. git push origin  upstream/release/v9.2

## 在Git Bash界面按步骤获取公钥
   //1.输入以下命令不断回车
   ssh-keygen -t rsa
   //2.获取公钥
   cat ~/.ssh/id_rsa.pub
## 将获得的公钥放到github 的SSH and GPG keys 的配置中
## 验证是否配置成功
    ssh -T git@github.com

## 要克隆带有子模块的 Git 仓库，可以使用以下命令：
~~~
bash
git clone --recurse-submodules <repository-url>
这个命令会克隆主仓库及其所有子模块。如果你已经克隆了主仓库但未更新子模块，可以运行：

bash
git submodule update --init --recursive
这会初始化并更新所有子模块。
~~~

## git 使用 Clash 代理
~~~
git config --global http.proxy 'http://127.0.0.1:7890'
git config --global https.proxy 'http://127.0.0.1:7890'
~~~


