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