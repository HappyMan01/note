## 丢弃修改
1. git checkout -- hello.txt
> 针对的是工作区(还没有add的)，相对于暂存区的内容来丢弃工作区的更改,**更改丢弃掉了**

2. git reset HEAD hello.txt
> 针对的是暂存区(add后的文件),将之前添加的缓存区的内容拉回到工作区,**更改还在**
