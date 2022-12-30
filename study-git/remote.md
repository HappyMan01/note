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
