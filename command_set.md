# 常用命令集合

## git

```shell
## 创建仓库
# …or create a new repository on the command line
$ echo "# dev" >> README.md
$ git init
$ git add README.md
$ git commit -m "first commit"
$ git branch -M main
$ git remote add origin https://github.com/xxx/dev.git
$ git push -u origin main

# …or push an existing repository from the command line
$ git remote add origin https://github.com/xxx/dev.git
$ git branch -M main
$ git push -u origin main

#####################################################################################################################################################
## 分支管理
# 查看本地所有分支
$ git branch
# 查看远程所有分支
$ git branch -r
# 查看本地和远程的所有分支
$ git branch -a
# 创建新分支
$ git branch <branchname>
# 切换分支
$ git checkout <branchname>
# 更新远程分支
$ git push -u origin <branchname>
# 拉取远程分支
$ git fetch origin <branchname> # git fetch是将远程主机的最新内容拉到本地，用户在检查了以后决定是否合并到工作本机分支中
$ git pull origin <remotebranch>:<localbranch> # 将远程主机的某个分支的更新取回，并与本地指定的分支合并，即：git pull = git fetch + git merge，这样可能会产生冲突，需要手动解决
$ git pull origin <remotebranch> # git pull是将远程主机的最新内容拉下来，直接与当前分支合并合并，冒号后面的部分可以省略
# 删除远程分支
$ git push origin --delete <branchname>
# 删除本地分支
$ git branch -d <branchname>
# 重命名本地分支
$ git branch -m <oldbranch> <newbranch>
```