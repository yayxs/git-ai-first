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

```sh
更新远程的分支
 git pull <remote> <branch>
 git pull origin main
``

## 很棒的 github 项目

- [https://github.com/pcottle/learnGitBranching](https://github.com/pcottle/learnGitBranching)

- [https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf/related](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf/related)

- [https://github.com/521xueweihan/git-tips](https://github.com/521xueweihan/git-tips)
```
