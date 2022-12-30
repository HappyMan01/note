## 远程
我们需要把我们本地仓库内容推送到远程以便能够更好的保存起来，或者给别人或者自己去观看

### 操作
- 添加远程仓库
```
git add remote orign https://github.com/HappyMan01/note.git
```
`origin` 是对远程地址的别名

- 推送到远程仓库
```
git push -u origin master
```
`-u` 表示把本地仓库和远程仓库关联起来，下一次只要git push就可以无需参数

- 拉去远程仓库
```git
#  拉去所有远程分支
git pull
```
- 拉去指定远程仓库指定分支
```
git pull origin test
```

- 查看远程仓库
```
# 展示远程别名
git remote show

# 展示远程仓库的主要信息
git remote show origin
```
- 查看远程仓库信息
```
git remote show origin
```
- 创建远程分支
```
创建并切换分支，add,commit，git push -u origin  dev
```
`-u` 映射远程dev和本地dev分支

- 删除远程分支
```
git push origin --delete dev
```
- 克隆远程指定分支
```
git clone https://github.com/HappyMan01/xxx.git  分支的名字(dev/master)
```
- 本地没有远程有分支
当我们克隆项目的时候有三个分支(master,dev,test),但是我们克隆之后本地没有dev,test分支，我们想要建立连接：
```
# 创建并切换分支基于origin/dev 分支
git checkout -b dev [origin/dev]
git checkout -b test [origin/test]
```
- 远程没有本地有分支
我们在远程没有的分支上直接git push会出现错误:
```
fatal: The current branch test has no upstream branch.
To push the current branch and set the remote as upstream, use

    # 建立本地test和远程test关联并推送到远程
    git push --set-upstream origin test

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```
`git push -u origin test` 和上面命相同
