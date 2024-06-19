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
image = "the-creative-exchange-d2zvqp3fpro-unsplash.jpg"
+++

### Git常用命令
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

### Git 关联 GitHub
#### 打开Git Bash,设置用户信息
    git config --global user.name "名字"
    git config --global user.email "邮箱"
#### 查看已配置的信息
    git config --global user.name
    git config --global user.email

#### 在Git Bash界面按步骤获取公钥
   //1.输入以下命令不断回车
   ssh-keygen -t rsa
   //2.获取公钥
   cat ~/.ssh/id_rsa.pub
### 将获得的公钥放到github 的SSH and GPG keys 的配置中
### 验证是否配置成功
    ssh -T git@github.com



#### 重新设置远程仓库地址: git remote set-url origin git@github.com:username/repository.git
#### 
