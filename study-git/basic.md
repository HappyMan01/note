## git
git是一个开源的分布式的版本控制系统，和集中式的版本控制不同的是它没有中央服务器的说法，每一个人的电脑上都是一个完整的版本控制系统.

### git的基本命令
1. git init

初始化一个空的git仓库

2. git status
查看版本库中文件的状态

2. git add file
追踪一个文件把文件添加到暂存区(stage)

3. git rm  file
误提交了某个文件可以使用git rm 和系统rm来恢复操作

4. git rm 执行两部操作，首先删除一个文件，把被删除的增加到暂存区;
**恢复**
  1. 从暂存区恢复到工作区 == git reset HEAD file<...>
  2. 在工作区撤销删除操作 git checkout -- file<...>

5. rm 操作删除了文件并没有纳入到暂存区,此时提交是提交不了的,还要add操作在提交,
我们可以直接使用git checkout -- file<...>来恢复这个文件

**如果删除文件使用git rm --cached file<...> 然后commit删除信息即可**

- git log
查看仓库提交的版本信息(作者时间消息ID...)
  - git log -3 仅展示当前最近3个提交日志
  - git log --pretty=oneline 一行展示日志信息
  - git log --pretty=reference 一行展示短id和提交消息

7. git commit -m "..."
提交文件到版本库

8. git config 
git config 可以配置用户名和邮箱(告诉git我们的身份),可以从三个地方更改这个配置

  * /etc/gitconfig ==> 系统级别(所有用户都有效) git config --system ...
  * ~/.gitconfig ==> 当前用户(只对当前用户有效) git config --global ...
  * .git/config ===> 当前仓库(或者项目有效) git config --local ...

9. git commit --amend -m '...'
修正上次提交的信息

10. git commit -adm '...'
git add 和 git commit 的简写

