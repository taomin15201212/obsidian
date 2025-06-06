在fork中直接用账号密码: username:password@hostname  拼接生成url ,  得到拼接url为:[http://username:123456@132.1.2:8002/git/product/backend/openapiclient.git](http://username:123456@132.1.0.2:8002/git/product/backend/openapiclient.git)  

  

https://username:password@gitlab.company.com/group/project.git  

http://root:QAZxsw!123@10.158.125.37:8280/gourp_1/sub_project_1.git  

SSH公钥生成

[https://blog.csdn.net/oliver486/article/details/126278011](https://blog.csdn.net/oliver486/article/details/126278011)

  

ssh-keygen -t rsa -C "gitlab_admin_9e8756@example.com" -f ~/.ssh/id_rsa_gitlab  

  

git config --global --get http.proxy 

没有任何显示，则你当前没有配置代理。之后我们需要输入

git config --global http.proxy 127.0.0.1:29290  

  

Git提交代码的流程

Pull Request:

1. Fork 代码!
2. 创建自己的分支: `git checkout -b feat/xxxx`
3. 提交你的修改: `git commit -am 'feat(function): add xxxxx'`
4. 推送您的分支: `git push origin feat/xxxx`
5. 提交`pull request`

  

- `feat` 增加新功能
- `fix` 修复问题/BUG
- `style` 代码风格相关无影响运行结果的
- `perf` 优化/性能提升
- `refactor` 重构
- `revert` 撤销修改
- `test` 测试相关
- `docs` 文档/注释
- `chore` 依赖更新/脚手架配置修改等
- `workflow` 工作流改进
- `ci` 持续集成
- `types` 类型定义文件更改
- `wip` 开发中
  

Git bash 执行命令

在需要上传的文件夹，右击 ，使用“Git bash”打开，便会进入该文件夹的当前目录

  

执行命令如下：
git add .
git commit -m "第一次提交"
git branch -M main
git remote add origin https://github.com/taomin15201212/obsidian.git
git push -u origin main


git init #若该文件尚未上传至Github过，则没有.git文件，需要执行该命令
git add . （注：别忘记后面的.，此操作是把Test文件夹下面的文件都添加进来）
git commit -m "提交信息" （注：“提交信息”里面换成你需要，如“first commit”）
git branch -M main（error: src refspec main does not match any 没有名为 `main` 的分支）
git remote add origin [git@github.com:taozhi1010/nest-admin.git](mailto:git@github.com:taozhi1010/nest-admin.git)  （git remote add 源项目别名（自己随便命名） git提供的ssh地址  ）
git remote add upstream GitUrl  
git push -u origin main （注：此操作目的是把本地仓库push到github上面）


git pull --rebase origin main （先拉远程再推送）
git push -u origin main

————————————————

[https://blog.csdn.net/weixin_41862755/article/details/123010189](https://blog.csdn.net/weixin_41862755/article/details/123010189)

  

### 常用命令及用法一览：

当电脑第一次使用（意思是输入一次，本电脑终身有用）：

1. git init  //git 初始化 （进本地目录以后）  
    

2. git remote add origin url     //url : 新建工程的url  
    

  

  

提交：

1. git add .   //本目录下所有修改工程提交至本地仓库  
    

2. git commit -m "up"  //必须步骤，为更新做描述  
    

3. git push origin master  //将本地仓库更新至远程仓库  
    

  

  

添加新文件：

1. git add .     //添加本目录下所有新添加的文件  
    

2. git commit -m "up"  //描述添加文件  
    

3. git push origin master   //更新  
    

删除文件：

1. git add .   //添加本目录下所有新更新的文件  
    

2. git commit -m "de"    //描述文件  
    

3. git rm "文件"    //删除文件  
    

4. git push origin master //更新  
    

下载工程：

1. git clone url   //url 是远程url  
    

远程相对本地的更新：

1. git pull origin master  
    
2. [https://www.cnblogs.com/snowlove/p/6095673.html](https://www.cnblogs.com/snowlove/p/6095673.html)
    

  

第一种方法：（简单易懂）

1、git add .（后面有一个点，意思是将你本地所有修改了的文件添加到暂存区）

2、git commit -m""(引号里面是你的介绍，就是你的这次的提交是什么内容，便于你以后查看，这个是将索引的当前内容与描述更改的用户和日志消息一起存储在新的提交中)

3、git pull origin master 这是下拉代码，将远程最新的代码先跟你本地的代码合并一下，如果确定远程没有更新，可以不用这个，最好是每次都执行以下，完成之后打开代码查看有没有冲突，并解决，如果有冲突解决完成以后再次执行1跟2的操作

4、git push origin master 将代码推至远程就可在fork中直接用账号密码: username:password@hostname  拼接生成url ,  得到拼接url为:[http://username:123456@132.1.2:8002/git/product/backend/openapiclient.git](http://uponline.geo-k.cn:8002/git/product/backend/openapiclient.git)以了

  

第二种方法：

1、git stash （这是将本地代码回滚值至上一次提交的时候，就是没有你新改的代码）

2、git pull origin master（将远程的拉下来）

3、git stash pop（将第一步回滚的代码释放出来，相等于将你修改的代码与下拉的代码合并）

然后解决冲突，你本地的代码将会是最新的代码

4、git add .

5、git commit -m""

6、git push origin master

这几步将代码推至了远程

最后再git pull origin master 一下，确保远程的全部拉下来

  

[https://blog.csdn.net/yuanmengdage/article/details/89881819](https://blog.csdn.net/yuanmengdage/article/details/89881819)

  

1.通过命令窗口

a. 打开你的 git bash 窗口

b. 进入 .ssh 目录：cd ~/.ssh

c. 找到 id_rsa.pub 文件：ls

d. 查看公钥：cat id_rsa.pub 或者 vim id_rsa.pub

  

生成公钥SSH

ssh-keygen -t rsa -C "taomin15201212@126.com"

三次回车，即可生成 ssh key

cat ~/.ssh/id_rsa.pub

ssh -T git@gitee.com

  

git clone url

git pull origin master 更新代码

  

git branch

git status

git rm test.py

git rm trst

git add

git commit -m

git push origin master

  

[https://www.bbsmax.com/A/kvJ3LpDA5g/](https://www.bbsmax.com/A/kvJ3LpDA5g/)

[https://www.cnblogs.com/txx403341512/p/9528528.html](https://www.cnblogs.com/txx403341512/p/9528528.html)

  

1.保留你本地的修改

git merge --abort

git reset --merge

合并后记得一定要提交这个本地的合并

然后在获取线上仓库

git pull

  

2.down下线上代码版本,抛弃本地的修改

不建议这样做,但是如果你本地修改不大,或者自己有一份备份留存,可以直接用线上最新版本覆盖到本地

git fetch --all

git reset --hard origin/master

git fetch

  

  

```
git pull origin master
```

然后再切换到对应的分支，

 git merge master

  

  

## 一、在dev分支上运行以下命令

　　`1. git add . // 暂存所有更改`

　　`2. git commit -m "更改的备注信息" // 将修改 提交到本地仓库，双引号内是提交的备注信息`

　　`3. git pull origin dev // 拉取远程dev分支代码`

　　`4. git push origin dev // 将本地修改的代码提交到远程的dev分支上`

　　`5. git checkout master // 切换到master分支`

## 二、在master分支上运行以下命令

　　`1. git merge dev // 将dev分支的代码合并到master上`

　 `2. git push origin master // 将当前的更改推送到远程的master分支上`

`执行完以上命令，此时dev分支与master分支的代码已同步。`

## 三、可能用到的命令

　　 1.  git checkout  // 可以看到当前的所处的分支位置，位于master还是dev等。  
　　2.  git log  // 可以看到近期的相关提交日志（提交时候的备注等）  
　　3.  git status  // 可以看到当前的文件状态 （如xx文件被修改，但未提交等）

  

```
git checkout remote/branch-name
```

```
git branch -a
```



npx degit w3cj/hono-open-api-starter my-api
### **命令解析**​

1. ​**`npx degit`**​
    
    - `degit` 是一个工具，直接克隆 GitHub 仓库的最新代码（不包含 `.git` 历史记录），比 `git clone` 更轻量。
    - `npx` 会自动下载并运行 `degit`，无需提前安装。
2. ​**`w3cj/hono-open-api-starter`**​
    
    - 模板仓库地址：w3cj/hono-open-api-starter
    - 这是一个预设了 Hono 框架 + OpenAPI 规范的 Starter 项目，包含基础路由、Swagger UI 文档等配置。
3. ​**`my-api`**​
    
    - 自定义的项目目录名称（可替换为你想要的名称）。