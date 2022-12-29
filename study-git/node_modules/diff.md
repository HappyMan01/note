## diff
比较工作区，暂存区，commit之间的差别;

## 操作
1. 把暂存区和工作区比较:
```git
git diff hello.txt,输出的结构
- 表示的是源文件(暂存区的文件)
+ 表示的目标文件(工作区的文件)
```
2. 把提交commit和工作区比较:
```git
git diff coomit_id(HEAD) hello.txt,输出的结构
- 表示的是源文件(commit的文件)
+ 表示的目标文件(工作区的文件)
```
3. 把提交commit和暂存区比较:
```git
git diff --cashed coomit_id(HEAD) hello.txt,输出的结构
- 表示的是源文件(commit的文件)
+ 表示的目标文件(暂存去的文件)
```
