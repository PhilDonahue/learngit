#### Git简介
1.C语言编写
2.Linux打造
##### 集中式vs分布式
CVS及SVN都是集中式的版本控制系统，而Git是分布式版本控制系统
##### 创建版本库

1.使用命令git add <file>，注意，可反复多次使用，添加多个文件；
2.使用命令git commit -m <message>，完成。
```
$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."
```
```
Asus@LAPTOP-H19PA2CH MINGW64 ~/Desktop/learngit (master)

$ vi readme.txt



Asus@LAPTOP-H19PA2CH MINGW64 ~/Desktop/learngit (master)

$ git add readme.txt

warning: LF will be replaced by CRLF in readme.txt.

The file will have its original line endings in your working directory



Asus@LAPTOP-H19PA2CH MINGW64 ~/Desktop/learngit (master)

$ git commit -m"wrote a readme file"

[master (root-commit) d6d6321] wrote a readme file

 1 file changed, 2 insertions(+)

 create mode 100644 readme.txt

```
#### 时光穿梭机
- 要随时掌握工作区的状态，使用git status命令。
- 如果git status告诉你有文件被修改过，用git diff可以查看修改内容。
```
$ git diff readme.txt
$ git status
```
##### 关联远程库
- 要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
- 关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
- 此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
##### 克隆远程库

- 要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。
- Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。
