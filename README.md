## Git vs GitHub

很多人应该听说过Git和GitHub，简单说一下两者的区别：

- 类比日记本：Git是一个免费、开源的分布式版本控制系统：说白了可以理解为一个日记本。专门记录东西的。比如今天发生了啥，记录一下。
- Hub：GitHub是一个Hub。类似一个平台。你应该听说过PornHub。上边存放了很多片子。也是一样的道理。GitHub存放了世界各地的代码。

## 快速开始

不知道Git相关的知识算不算编程相关的。不过如果说你想利用AI编程，我觉得第一步应该是了解Git是什么。为什么这么说呢，因为它就像一个日记本一样记录了你代码的一生。同时也记录了你每天写的什么代码。这在未来都是一种财富。所以在AI时代，这是第一课。

既然说了两个名词，一个是Git，一个是GitHub。

- 你自己访问：https://github.com/ 这个网址注册一个属于你自己的账号。建议使用谷歌邮箱。当然如果说你不知道怎么注册，你都已经使用AI了，让AI帮你。那么或者一步步查询相关网上的资料。

- Git：这个东西就是安装在你的电脑中。https://git-scm.com/downloads 在这里下载Git。

特别说明：如果说上边两步你遇到了问题，请你自行AI。或者搜索信息就行。多一点耐心肯定能解决。

## 我与Git

首先我比较正确的一点，是我编程的早期，接触到了Git。然后也存放了很多自己的代码。所以我建议你，如果想编程。第一步应该是准备好Git和GitHub。不过我当时真的不知道什么意思。到底啥是Git呢。

## 一些工具 / 网站

- [GitButler 版本控制客户端 https://github.com/yayxs/git-learn](https://github.com/yayxs/git-learn) 由 Tauri/Rust/Svelte 提供支持

## Git 命令

#### git config 相关

```sh

git config user.name

git config user.email

git config --local user.name "yayxs"

git config --local user.email "yayxs@gmail.com"



git config --local --list  # 查看本地的config


```

### 重置

```sh
git reset # 取消 git add . 操作
```

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
