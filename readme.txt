Git is a version control system.
Git is free software
Git is a distributed version control system.
Git is free software distributed under the GPL
Git has a mutable index called stage.
Git tracks changes of files.

<name> 可以代表 readme.txt  也可以代表 dev
查看当前文件路径 pwd


初始化Git  git init
查看文件状态 git status
添加单个文件 git add <name>
提交文件 git commit -m “提交信息”
查看不同 git diff <name>
查看最近提交记录 git log
查看简版的提交记录 git log —pretty=oneline
查看历史命令  git reflog
回复之前的版本 git reset —hard HEAD^ //上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。
回复到指定版本 git reset —hard commit_id  //commit_id的就是那一堆乱码的前几位就行了
查看工作区和版本库里面最新版本的区别 git diff HEAD — <name>
撤销文件在工作区的全部修改  git checkout —- <name>
查看某个文件 cat <name>
删除一个文件 rm <name>
从版本库里删除一个文件 git rm <name>  //然后要进行提交操作




添加到远程仓库：git remote add origin <path> //这里的path代表远程地址
第一次push到远程分支：git push -u origin master  //把本地的master分支推送到远程
推送到远程分支 git push origin master //把本地master分支的最新修改推送到Github


git checkout -b dev //代表创建dev分支，然后切换到dev分支  -b参数表示创建并切换
git checkout -b dev  相当于 git branch dev  和 git checkout dev 

查看分支：git branch
创建分支 git branch <name>
切换分支 git checkout <name>
创建+切换分支 git checkout -b <name>
合并某分支到当前分支 git merge <name>
删除分支 git branch -d <name>

查看分支合并情况：git log —graph —-pretty=oneline —-abbrev-commit

合并分支的时保留记录 git merge —no-ff -m “合并信息” <name>


储存工作空间 git stash 
查看存储的工作空间 git stash list
恢复存储的工作空间 git stash apply <name> //如果有多个stash 可以检出指定的stash
删除stash存储空间的内容 git stash drop
恢复工作空间同时把stash内容也删除 git stash pop //如果stash多的话就还可以先list 然后检出



