创建一个目录作为 git 仓库：
 $ mkdir git-repository
 $ cd git-repository
初始化：
 $ git init

 $ git status 
 $ git diff < file name >
 $ git add < file name >
 $ git commit -m "commit description"
 $ git log
 $ git log --pretty=oneline
 $ git reset --hard HEAD^
 $ git reset --hard < commit id >
 $ git reflog
 $ git checkout -- < file name > 
 $ git reset HEAD < file name >
远程仓库
创建SSH Key
 $ ssh-keygen -t rsa -C "example@email.com"
 将在用户目录下生成.ssh 目录，其中包含id_rsa(私钥),id_rsa.pub(公钥)
与远程仓库建立关联
 $ git remote add origin git@github.com:yoenchen/gitskills.git
 $ git push -u origin master   -u:推送时，将远程 master 分支与本地 master 关联起来
 $ git push origin master
 $ git clone git@github.com:yoenchen/gitskills.git
分支
 $ git checkout -b dev 
 $ git checkout < branch >
 $ git branch
 $ git branch < name >
 $ git brand -d < branch >
 $ git merge < branch >
 $ git log --graph --pretty=oneline --abbrev-commit
 $ git merge --no-ff -m "message" < branch >
储藏工作现场
 $ git stash
 $ git stash list
 $ git stash apply
 $ git stash drop
 $ git stash pop 

 $ git branch -D < branch >   -D:强行删除分支
 $ git remote
 $ git remote -v 
 $ git push origin master 
 $ git pull
标签
 $ git tag 
 $ git tag < tag >
 $ git show < tag >
 $ git tag -a v1.0 -m "description" < commit id >    -a:描述标签信息
 $ git tag -d < tag >
 $ git push origin v1.0
 $ git push origin --tags  一次推送所有本地标签
 删除远程标签
 $ git tag -d v0.9
 $ git push origin :refs/tags/v0.9
