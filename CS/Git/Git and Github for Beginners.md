****

![[Pasted image 20240102142527.png]]

![[Pasted image 20240102142750.png]]

[Git and GitHub Tutorial for Beginners - YouTube](https://www.youtube.com/watch?v=tRZGeaHPoaw)

## 如何创建一个 git 库

有一个非常简单的方法：就是直接右击文件夹然后 git bash here ；他就会跳出来 git 那个终端，然后就表示 git 到达了这个文件夹（如果不右键 bash 的话，也可以直接用 cd 去找）

然后再

```
git init
```

![[Pasted image 20240102153458.png]]

这个时候 git 库就被创建好了，它会在我们本地这个文件夹里面创建一个隐藏的文件夹 .git ，这个文件

夹将记录我们的提交等巴拉巴拉一系列的操作；

![[Pasted image 20240102152550.png]]

![[Pasted image 20240102152615.png]]

## git 一些基本操作
---

![[Pasted image 20240102153538.png]]

```
git status
```

这个命令将会告诉我们当前 git 库中的操作情况

![[Pasted image 20240102153705.png]]

```
git add index.htm
```

意味着我们对 `index.htm` 这个文件进行了跟踪

当我们 `git rm --cached index.htm`

![[Pasted image 20240102153847.png]]

表示我们不再跟踪这个文件；

---

### .gitignore 文件的创立

在本地 git 库中我们可以手动创建一个 `.gitignore` 文件，由此我们可以使得 git库忽略掉在这个文件

中我们要求它忽略的文件；


![[Pasted image 20240102154410.png]]

```
# ignore all.txt files
*.txt
```

如上所写，我们可以使得 git 不再显示 txt 文件

![[Pasted image 20240102154517.png]]

---


```
git add --all
git add -A
git add .
```

这三个操作都可以使得跟踪所有 git 库中的文件

![[Pasted image 20240102155647.png]]

