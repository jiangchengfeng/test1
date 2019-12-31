### 基本使用

通过 `git clone` 命令下载远程仓库到本地
+ `git clone` 会自动帮你把远程仓库下载到本地 不需要再去 `git init` 了
+ 通过 `clone` 下来的仓库 `git` 有一个远程仓库地址列表 `git` 默认会把你 `clone` 的地址起一个别名:`origin` 然后你执行 `push` 的时候 实际上就是将本地的版本提交到 origin 上

在本地进行操作 通过 `git commit` 形成历史记录

通过 `git push` 将本地仓库中的历史记录提交到远程仓库

### 本地已有仓库 需要提交到线上
如果是 `git init` 出来的仓库 进行 `push` 提交的时候就不知道要往哪 push
所以 这里通过 `remote` 相关命令进行设置

```
# 查看远程仓库地址
- git remote show 
# 根据别名查看指定的远程仓库信息
- git remote show 远程仓库别名
# 添加远程仓库地址信息
- git remote add 远程仓库别名 远程仓库地址
# 提交
- git push 仓库地址别名 master
```
如果要省略 git push 后面需要指定的 `仓库别名master` 可以通过下面命令修改：

```
git push --set-upstream 仓库别名 `master`

```

## 初始化一个Git仓库
- git init 
## 查看当前工作区 暂存区 本地仓库的状态
- git status 
- git add
## 添加当前目录所有文件到暂存区
- git add all /git add . 
## 删除工作区文件 并且将这次删除放入暂存区
- git rm [file1][file2]... 
## 停止追踪指定文件 但该文件会保留在工作区
- git rm --cached [file]
## 改名文件 并且将这个改名放入暂存区
- git mv [file-original][file-renamed]
## 提交暂存区到仓库去
- git commit -m "日志说明"
## 提交工作区自上次commit之后的变化 直接到仓库去
- git commit -a
## 如果代码没有任何变化 则用来改写上一次commit的提交信息
- git commit --amend -m
- git log
- gitk

操作git的基本工作流程就是先修改文件 然后执行 git add 命令
git add命令会把文件加入到暂存区 接着就可以执行 git commit命令
将文件存入文档库 从而形成一次历史记录

## git-bash 常用命令

touch 创建文件
cat 查看文件
less 查看大文本文件  q退出
vi: visual interface 文本编辑 :q退出vi  i 插入 :w保存
pwd
ls 查看文件目录
ls -a  查看隐藏文件
mkdir
clear
rmdir +只能删除空目录
rm +文件名
rm -rf 目录名