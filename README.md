## 什么是 git

git 分布式版本管理系统
管理历史记录的数据库
本地数据库、远程数据库
远程数据库配有专门的服务器 多人共享建立的

## 简明指南

- [git 简明指南](https://rogerdudler.github.io/git-guide/index.zh.html)

```sh
创建本地仓库的克隆版本
远端服务器上的仓库
git clone https://github.com/yayxs/git-learn.git
```

工作流：工作目录 + 暂存区 + HEAD

```sh
添加到暂存区
git add <filename>
```

```sh
git commit -m "代码提交信息"
执行此命令后 改动已经提交到了 HEAD
```

```sh
git push origin main
提交到远程的main分支
```

```sh
git checkout -b feature_x


推送到远程的分支
git push origin feature_x
```

````sh
更新远程的分支
 git pull <remote> <branch>
 git pull origin main
``

```sh
创建tag
git tag 1.0.0  35df273
````

```sh
本地仓库的历史记录
git log

查看某一个人的记录
git log --author=yayxs

```

```sh
通过 ASCII 艺术的树形结构来展示所有的分支, 每个分支都标示了他的名字和标签
git log --graph --oneline --decorate --all
```

```sh
替换本地的改动 filename 是改动的文件名
git checkout -- <filename>
```

## 稍微复杂一点

```sh
使用远程最新的
git fetch --all && git reset --hard origin/main

Fetching origin
HEAD is now at 0d6ab89 远程的是最新的
```

```sh
git diff
工作区和暂存区的不同

展示本地仓库中任意两个 commit 之间的文件变动

git diff id1 id2
```

```sh
展示本地分支关联远程仓库

git branch -vv
```

```sh
所有的远程分支
git branch -r
origin/HEAD -> origin/main
  origin/feature1
  origin/feature_x
  origin/main
  origin/pr
  origin/rebase
```

```sh
远程分支和本地分支的对应关系
git remote show origin

删除本地的分支
git branch -d <local-branchname>
删除远程的分支
git push origin --delete <remote-branchname>
```

```sh
查看标签
git tag -ln
```

```sh
推送所有的标签
git push origin --tags
```

```
查看本地的config
git config --local --list
```

## 规范 Type

- [angular.js type](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type)

- feat: 一个新的功能
- fix: 错误修复
- docs: 仅仅文档修改
- style: 不影响代码的含义 空格 格式化 少分号等等
- refactor: 不修复错误 也没有新功能
- perf: 提高性能的代码修改
- test: 测试相关
- chore: 构建过程 辅助工具 库的更改

## .github

`.github` 目录通常在一个 GitHub 项目中使用，用于存放 GitHub 提供的一些特性和工具的配置文件。以下是 .github 目录中可能包含的一些文件或子目录：

- ISSUE_TEMPLATE 文件夹 :用于创建 issue 模板
- PULL_REQUEST_TEMPLATE 文件夹：用于创建 pull request 模板

## 很棒的 github 项目

- [learnGitBranching](https://github.com/pcottle/learnGitBranching)

- [refined-github](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf/related)

- [521xueweihan/git-tips](https://github.com/521xueweihan/git-tips)
