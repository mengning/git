# git
Git User Guider

## 第一关：Git本地版本库的基本用法
```
git init # 初始化一个本地版本库
git status # 查看当前workspace的状态
git add [FILES] # 把文件添加到index
git commit -m "wrote a commit log infro” # 把文件提交到仓库
git log # 查看commit的日志，查看当前HEAD之前的commit，可以回到过去
git reset —hard HEAD^^/HEAD~100/commit-id/commit-id的头几个字符
git reflow # 可以查看当前HEAD之后的commit，可以回到未来
git reset —hard commit-id/commit-id的头几个字符
```