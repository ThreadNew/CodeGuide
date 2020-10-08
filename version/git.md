### Git相关命令的操作示例

> **Tips**: Git和SVN的主要区别 Git是分布式而SVN是集中式

##### 一、本地代码库操作

---

##### 1、新建仓库

###### 1.1 git init

> 文件夹下会出现.git 文件夹

```java

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo
$ git init
Initialized empty Git repository in G:/git/gitDemo/.git/

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$

```

###### 1.2 git clone [url]

> 拷贝一份远程仓库或者下载一个项目

```java
hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git clone http://mob***eapi.gree.com:3000/*****/notebook.git
Cloning into 'notebook'...
remote: Counting objects: 42, done.
remote: Compressing objects: 100% (40/40), done.
remote: Total 42 (delta 13), reused 0 (delta 0)
Unpacking objects: 100% (42/42), done.

```

---

##### 2、提交

###### 2.1 git add [file]/[dir]/.

> git add 可将文件添加到暂存区；可以添加一个或多个文件也可以添加指定目录包括子目录以及当前目录的所有文件

```java
hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ ll
total 0

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ touch a.txt
hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        a.txt

nothing added to commit but untracked files present (use "git add" to track)

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git add a.txt

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   a.txt


```

###### 2.2 git commit -m [message]

> 将暂存区的内容添加到本地仓库中

```java
hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git commit -m "note"
[master (root-commit) be4b23f] note
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt

hase@DESKTOP-AVDSH46 MINGW64 /g/git/gitDemo (master)
$ git status
On branch master
nothing to commit, working tree clean

```

