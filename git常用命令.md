### Linux命令

git常用命令

cd 

pwd   当前所在的目录

ls 列出当前目录中的所有文件

touch 新建一个文件 例如 touch index.js

mkdir 新建一个文件夹

rm 删除一个文件 例如 rm index.js

rm -r 删除一个文件夹 例如 rm -r src 删除src文件夹

//切物rm -rf 删除电脑中所有文件

mv index.js src 相当于把index.js移动到 src目录下

clear 清屏

histroy 查看历史命令



### git 配置

git config --global --list



![image-20210621215318664](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210621215318664.png)

可以修改user.name 和user.emai 相关的配置 ， 必须配置

git config --system --list

### git提交

1.git init 初始化

2.在git相应的目录下写文件代码，然后git add将文件从工作区添加到暂存区，也可以用git rm --cached 文件名   把文件从暂存区中删除，删除只是删除了暂存区的文件，工作区中该文件还存在只不过没有被git所管理 git checkout 文件名 将暂存区中的文件覆盖工作区的文件

git status查看有没有添加到暂存区的文件

 3.然后再git commit -m“这边写提交的相关信息” 提交到仓库中。  也可以 通过git reset --hard  加上一串之前提交的   可以用本低仓库覆盖上那次提交。 

 ![image-20210622102741815](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622102741815.png)

git log 可以查看提交到仓库的历史记录

### git分支命令

主分支->开发分支->功能分支

git check 查看分支

git branch 分支名称  创建分支

git checkout 分支名称 切换分支

git merge 分支名称 实现合并分支

git branch -d（D） 分支名称 实现删除分支 大D实现强制删除分支

在一个分支上创建一个文件然后add到缓存区 然后切换分支，那这个文件就会被携带到其他分支上去，所以得 git commit 文件名-m 然后切换， 但是也可以 

git stash 将改动存储起来

git stash pop 将改动从存储中提取出来



### 本地仓库和远程仓库

#### 程序员A：

push到远程仓库：git push https://github.com/842180800/git-demo.git master

可以给远程仓库起一个名字  

git remote add origin https://github.com/842180800/git-demo.git

就可以直接git push origin master

![image-20210622120314613](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622120314613.png)

![image-20210622120805276](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622120805276.png)

之后下次提交就可以直接 git push

![image-20210622121257051](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622121257051.png)

#### 程序员B

先 git clone 下项目，然后将修改完的代码 git push到远程仓库中

#### 程序员A

程序员A就可以git pull将程序员B更新好的代码拉下来这就是最新代码版本

git pull 是本地仓库本来就存在项目，然后将新的代码和本低仓库进行比较

如果远程仓库的版本比本地仓库的版本高的话，必须拉去远程仓库的最新版本到本地仓库在进行提交。

### 解决冲突

程序员A先修改了一个文件的一个地方提交了，而程序员二也修改了这个地方但是提交不成功

程序员B需要git pull origin master 拉到本地再 git push

### SSH免登录方式

![image-20210622133706851](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622133706851.png)

![image-20210622133725431](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20210622133725431.png)
