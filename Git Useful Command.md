## Git Useful Command

#### 查看Git版本

```
git version
```

#### 代码开发流程

1.提交代码给本地库

2.将代码提交到Git远程库

3.从远程库获取最新代码

4.继续修改编代码



#### Git基础概念

1.本地工作文件夹：任何文件夹都是

2.Git索引区（stage）：在没有提交给本地库时代码的位置，先提交给索引区

3.Git库（Repository）：提交给本地库的代码 （本地库，远程库）



#### Git 设定

1.建立Git库

```
git init
```

2.设置基础信息

```
git init
git config -l //查看当前信息
git config --global user.name "haha" //全局用户名设置
git config --global user.email "haha@email.com" //全局用户名设置
git config -l //再看一下设置是否正确
```

3.帮助命令

```
git config --help
git help config
git help commit ...
```



#### Git提交

1.建立文件夹

```
mkdir hahaha
cd hahaha
```

2.建立本地仓库并初始化

```
git init
```

3.创建/编辑文件

4.查看状态

```
git status   //显示红色的文件即为修改过，还未放到索引区
```

5.添加到索引区

```
git add xxx.cpp
```

6.再次查看状态

```
git status  //显示绿色文件，修改过后已经放到索引区
```

7.向本地库提交

```
git commit -m "what have you done"
```

8.查看提交历史

```
git log
git log --oneline  //一行显示
git log -p  //显示更加详细
```



#### Git状态

1.查看当前文件夹状态

```
git status
```

2.恢复上一个版本的文件（此时还没有提交到索引区）

```
git checkout -- xxx.cpp  //迁出
```

3.查看状态

```
git status  //此时文件修改内容消失
```

4.如果已经添加到索引区

```
git reset HEAD xxx.cpp  //退出移除索引区
```

5.再用checkout取消

```
git checkout -- xxx.cpp  //迁出
```



#### 比较修改内容

1.工作文件夹比较

```
git diff  //绿色显示增加一行
```

2.添加到索引区

```
git add xxx.cpp
```

如果已经添加岛索引区，此时无法使用 git diff；无法比较工作文件夹的修改文件

4.索引区比较

```
git diff --cached
```



#### 文件操作

1.添加文件

```
git add [file1 file2 ...]
git add .
```

2.删除

```
git rm
```

如果已经在索引区

```
git rm --cached xxx.cpp
```

3.文件改名

```
git mv xxx.cpp hhh.cpp
```



#### 使用分支

1.查看当前分支状态

```
git branch
```

2.开新分支dev

```
git branch dev
```

3.切换到新的分支

```
git checkout dev
```

4.修改文件，此时在开发分支

5.提交，此时在开发分支

```
git add .
git commit -m "Fixed Bugs"
```

6.查看开发履历

```
git log
```

7.切换回主分支

```
git checkout master
```

8.查看状态

```
git log
git branch
```

9.合并主分支

```
git merge dev
```

10.再次查看状态

```
git log
```

11.删除之前的开发分支

```
git checkout -d dev
```

12.再次查看状态

```
git branch
```

