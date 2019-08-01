Git的基本命令：
git log
git status
git add .
git commit -m XX文件
rm XX文件
git reset --hard HEAD~n  回退n个版本
git checkout -- XX文件  恢复已删除的文件
git push origin master  把master给到origin去

Git分支创建命令：
git checkout -b XX分支   新建并切换到该分支
git branch  查看分支列表
git branch XX分支   创新xx分支但不切换当前分支
git checkout XX分支  切换到xx分支
git branch -d XX分支   删除xx分支
在分支1中键入： git merge 分支2   即将分支2的内容合并到分支1中


当Git分支合并发生冲突时的解决方法：
首先合并分支 git merge
但显然会错误，因为冲突了
这时直接进入该文件，改好了就可以git add &commit了

分支debug策略：
碰到一个bug就新开一个分支，然后修改成功后，再合并到master分支中
如果一个分支还没有修改完不能commit的时候，使用git stash隐藏当前工作现场（相当于把工作现场压入缓存）
然后等下次想要继续修改时，使用git stash pop，来恢复工作现场
