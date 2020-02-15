# Git User Guider

## 第一关：Git本地版本库的基本用法
```
git init # 初始化一个本地版本库
git status # 查看当前workspace的状态
git add [FILES] # 把文件添加到index
git commit -m "wrote a commit log infro” # 把文件提交到仓库
git log # 查看commit的日志，查看当前HEAD之前的commit，可以回到过去
git reset —hard HEAD^^/HEAD~100/commit-id/commit-id的头几个字符
git reflog # 可以查看当前HEAD之后的commit，可以回到未来
git reset —hard commit-id/commit-id的头几个字符
```

## 第二关：Git远程版本库的基本用法
```
git clone https://github.com/YOUR_NAME/REPO_NAME.git # 通过clone远端的版本库从而在本地创建一个版本库，需要您先在github.com上注册账号并创建一个版本库
git commit / git reset —hard / git log等本地repo的操作
这里使用默认远程origin/master和本地master，没有创建其他分支
git remote -v # 查看远程库信息
git pull # 将远程repo更新到本地，实际上是git fetch + git merge
git push # 将本地commit更新到远程repo
```
## 第三关：Git分支合并
```
git pull # 将远程repo更新到本地，实际上是git fetch + git merge
git branch
git checkout -b mybranch # 创建自己的工作分支
git add/git commit A2/A3
git checkout master
当其他小伙伴在你git push之前已经更新过远程repo，这时你git push时可能会失败，因为在master上发生了分叉，要首先git pull。
git merge mybranch # 将自己的工作合并到master，并尽快更新到远程repo。如果不幸其他小伙伴的更新和你本地的commit有冲突（都修改了同一位置），需要先处理冲突
git push # 将本地commit更新到远程repo，
```
## 第四关：Git Rebase
```
在分支上完成自己的工作之后，为了让log记录将来更容易回朔参考，需要用git rebase重整一下
git pull # 将远程repo更新到本地，实际上是git fetch + git merge
git checkout -b mybranch # 创建自己的工作分支
git add/git commit A2/A3。。。
git rebase
git rebase --continue
git checkout master
git pull
git merge mybranch
git push # 将本地commit更新到远程repo
```
