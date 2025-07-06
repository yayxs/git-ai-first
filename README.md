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

回想起我早期编程的时候，接触到了Git。然后也存放了很多自己的代码。所以我建议你，如果想编程。第一步应该是准备好Git和GitHub。不过我当时真的不知道什么意思。到底啥是Git呢。其实之前还是通过看视频的方式学习。

工作了很多年，即使到了现在，仍然有很多Git的使用不会。不过，这都将不重要。因为有了AI。

自己习惯把自己的一些代码案例放在GitHub上一方面是记录学习，最重要的一点就在在未来的某天看看现在写的代码，在现在去总结过去写的代码。

## 打个比方

看到这的时候，就要有个概念了。什么概念呢，仓库。我们在电脑写的文本、或者代码、或者任何自然语言应该是放在一个文件夹中。可以把这个文件夹当作一个仓库。我们可以往这个仓库中存东西，取出东西。不过需要记住的是在远程也有一个仓库。也可以往远程的仓库放东西，取出东西。

## 规范

每一次commit 都像是回答你女朋友的问题，不知道如何更好的描述自己的这次提交信息。当你在看一个开源的项目的时候，会看到commit的信息会比较规范。但是总的来讲是这么几类。一个良好、统一的Git提交信息（Commit Message）规范对于团队协作、代码维护、版本回滚以及自动生成更新日志（Changelog）都至关重要。

目前，社区中最流行和广泛使用的是 Conventional Commits（约定式提交）规范。它的格式非常结构化，也易于被机器解析。

```
`type` (类型): 用于说明本次提交的类别。常见的类型有：
       * feat: 新功能 (feature)
       * fix: 修复 Bug
       * docs: 仅仅修改了文档 (documentation)
       * style: 代码格式修改，不影响代码逻辑 (比如修改空格、分号等)
       * refactor: 代码重构，没有新增功能或修复 Bug
       * test: 增加或修改测试用例
       * chore: 构建过程或辅助工具的变动 (比如修改 .gitignore)
       * perf: 提升性能的改动
       * revert: 回滚上一个提交
```

当然，现在有些团队，使用和AI每次对话时候的自然语言作为Commit信息。Cloudflare的一个开源项目 workers-oauth-provider，几乎完全由AI生成，项目作者在每个commit中都附上了用到的prompt。

## Git Config

```sh
git config user.name # 查看当前的用户名

git config user.email # 查看当前的邮箱

git config --local user.name "yayxs" # 设置本地的用户名

git config --local user.email "yayxs@gmail.com" # 设置本地的邮箱

git config --local --list  # 查看本地的config
```

## Git Reset

```sh
git reset # 取消 git add . 操作
```

## Git Guide

> [git 简明指南](https://rogerdudler.github.io/git-guide/index.zh.html)

```sh
# 创建本地仓库的克隆版本
# 远端服务器上的仓库
git clone https://github.com/yayxs/git-learn.git
```

工作流：工作目录 + 暂存区 + HEAD

```sh
# 添加到暂存区
git add <filename>
```

```sh
git commit -m "代码提交信息" #执行此命令后 改动已经提交到了 HEAD
```

```sh
git push origin main #提交到远程的main分支
```

```sh
git checkout -b feature_x
# 推送到远程的分支
git push origin feature_x
```

````sh
# 更新远程的分支
 git pull <remote> <branch>
 git pull origin main
``

```sh
# 创建tag
git tag 1.0.0  35df273
````

```sh
#本地仓库的历史记录
git log

# 查看某一个人的记录
git log --author=yayxs

```

```sh
# 通过 ASCII 艺术的树形结构来展示所有的分支, 每个分支都标示了他的名字和标签
git log --graph --oneline --decorate --all
```

```sh
# 替换本地的改动 filename 是改动的文件名
git checkout -- <filename>
```

## 稍微复杂一点

```sh
# 使用远程最新的
git fetch --all && git reset --hard origin/main

Fetching origin
HEAD is now at 0d6ab89 远程的是最新的
```

```sh
git diff
# 工作区和暂存区的不同

# 展示本地仓库中任意两个 commit 之间的文件变动

git diff id1 id2
```

```sh
# 展示本地分支关联远程仓库

git branch -vv
```

```sh
# 所有的远程分支
git branch -r
origin/HEAD -> origin/main
  origin/feature1
  origin/feature_x
  origin/main
  origin/pr
  origin/rebase
```

```sh
# 远程分支和本地分支的对应关系
git remote show origin

# 删除本地的分支
git branch -d <local-branchname>
# 删除远程的分支
git push origin --delete <remote-branchname>
```

```sh
# 查看标签
git tag -ln
```

```sh
# 推送所有的标签
git push origin --tags
```

## .github

`.github` 目录通常在一个 GitHub 项目中使用，用于存放 GitHub 提供的一些特性和工具的配置文件。以下是 .github 目录中可能包含的一些文件或子目录：

- ISSUE_TEMPLATE 文件夹 :用于创建 issue 模板
- PULL_REQUEST_TEMPLATE 文件夹：用于创建 pull request 模板
