## [Git](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

### 常用Git指令
指令 | 释意
-------|-------
git init | 初始化仓库
git clone | 克隆仓库
git status | 查看状态
git add (file name) | 添加文件至暂存区
git add -f (file name) | 强制添加文件至暂存区（文件被.gitignore忽略）
git add -p (file name) | 暂存文件某些修改后添加文件至暂存区
git diff (file name) | 查看工作区文件与仓库文件差异
git rm (file name) | 删除文件并将删除记录添加至暂存区
git commit -m (message) | 提交修改记录
git log | 查看提交日志
git log --all | 显示所有分支提交日志
git log --graph | 图形方式查看提交日志
git log --pretty=oneline | 压缩方式查看提交日志
git log --abbrev-commit | 简化方式查看提交日志
git reflog | 查看所有操作日志（包括仓库被reset --hard后的日志）
git reset --hard (commit id) | 重置仓库至某次提交
git reset HEAD (file name) | 重置暂存区文件至工作区
git checkout -- (file name) | 放弃工作区某个文件修改记录
git checkout (branch name) | 切换分支
git checkout -b (branch name) | 切换并创建新分支
git pull | 拉取远程记录并自动合并
git fetch | 拉取远程记录不执行自动合并
git branch | 查看所有分支
git branch (branch name) | 创建新分支
git branch -d (branch name) | 删除分支
git branch -D (branch name) | 强制删除分支（丢弃分支记录）
git branch --set-upstream (branch name) origin/(branch name) | 创建本地分支和远程分支链接关系
git merge (branch name) | 合并分支到当前分支
git merge --no-ff -m (message) (branch name) | 不启用fast forward模式合并分支到当前分支
git stash | 暂存修改记录
git stash list | 查看暂存修改记录列表
git stash apply (stash name) | 恢复暂存修改记录但不从暂存修改记录列表中移除此次暂存记录
git stash drop (stash name) | 从暂存修改记录列表中移除此次暂存记录
git stash pop (stash name) | 恢复暂存修改记录并从暂存修改记录列表中移除此次暂存记录
git remote | 获取远程仓库信息
git remote -v | 获取远程仓库详细信息
git tag | 查看所有标签
git tag (tag name) | 在当前记录上创建标签
git tag (tag name) (commit id) | 在某次记录上创建标签
git tag -d (tag name) | 删除标签
git tag -a (tag name) -m (message) (commit id) | 在某次记录上创建带说明标签
git tag -s (tag name) -m (message) (commit id) | 在某次记录上用PGP签名标签
git show (tag name) | 查看标签信息
git show (commit id) | 查看某次提交修改记录
git push origin (branch name) | 推送本地记录至远程仓库
git push -u origin (branch name) | 推送本地记录至远程仓库并创建本地分支和远程分支链接关系
git push origin (tag name) | 推送本地标签至远程仓库
git push origin --tags | 推送全部尚未推送到远程仓库的标签至远程仓库
git push origin :refs/tags/(tag name) | 删除远程标签（前提先删除本地标签）
git config --global color.ui true | 以彩色形式显示git记录
git config --global alias.(short name) (action name) | 配置git操作命令简写
git check-ignore -v (file name) | 检查文件的忽略规则
git cherry-pick (commit id) | 提取某次提交记录到当前分支
git cherry-pick -x (commit id) | 提取某次提交记录到当前分支并保留原提交者信息
git cherry-pick (start commit id)..(end commit id) | 提取从start commit id到end commit id的所有提交记录到当前分支（不包含start commit id）
git cherry-pick (start commit id)^..(end commit id) | 提取从start commit id到end commit id的所有提交记录到当前分支（包含start commit id）
git blame (file name) | 显示某个文件每一行修改记录
git fsck --lost-found | 查看丢弃的提交
git rebase -i HEAD~(number of commits) | 压缩最后几次提交
git rebase -i HEAD~~ | 压缩过去所有提交
git rebase (branch name) | 将某分支的最新的那些提交改变为当前分支的基础
git rebase --continue | 解决rebase冲突后继续进行rebase操作（解决rebase冲突后需要先执行git add命令，再执行此命令）
git rebase --skip | 发生rebase冲突后，跳过冲突的补丁
git rebase --abort | 发生rebase冲突后，停止rebase操作

### 常用Git指令缩写

```
add-f = add -f
add-p = add -p
br = branch
br-d = branch -d
br-D = branch -D
cfg = config
cmt = commit
cmt-m = commit -m
co = checkout
co-b = checkout -b
co-r = checkout --
cp = cherry-pick
cp-a = cherry-pick --abort
cp-c = cherry-pick --continue
cp-s = cherry-pick --skip
cp-x = cherry-pick -x
fsk = fsck --lost-found
log-a = log --all
log-g = log --graph
log-z = log --pretty=oneline
log-s = log --abbrev-commit
mg = merge
mg-nfm = merge --no-ff -m
push-o = push origin
push-uo = push -u origin
push-t = push origin
push-ts = push origin --tags
rbs = rebase
rbs-a = rebase --abort
rbs-c = rebase --continue
rbs-s = rebase --skip
reset-f = reset --hard
reset-h = reset HEAD
st = status
sts = stash
sts-a = stash apply
sts-c = stash clear
sts-d = stash drop
sts-l = stash list
sts-p = stash pop
tag-d = tag -d
tag-a = tag -a
tag-s = tag -s
```
