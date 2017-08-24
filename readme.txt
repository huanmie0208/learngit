git使用常用命令
git add readme.txt
git commit -m "xxx"
git log
git diff
git log --pretty=oneline
git status
git reset --hard HEAD^^  /*^代表上个版本,^^上上个版本
git reflog
git reset --hard  9d7c4bd 回退到某版本
cat readme.txt
git diff HEAD -- reame.txt
git checkout -- readme.txt
/**
命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。
**/
git clone git@github.com:你的用户名/库名.git  克隆自己的远程库
git push origin master  提交
git checkout -b dev  创建分支并切换 相当于 git branch dev  |git checkout dev
git branch 查看分支,当前分支前有*号
git checkout master  切换到master分支

***git merge --no-ff -m "merge with no-ff" dev
git log --graph --pretty=oneline --abbrev-commit  合并后查看分支历史

git merge dev 合并dev到当前分支
git branch -d dev  删除dev分支
git branch 查看

git stash	将工作现场储藏
git stash list   查看工作现场
	两种恢复工作方式
	git stash apply   恢复后,stash不删除,需要git stash drop 来删除
	git stash pop  恢复的同时把stash也删了
git stash apply stash@{0}  恢复指定的stash
git branch -D features-vulcan  强行删除features-vulcan分支
git remote 查看远程库的信息  git remote -v 显示更详细的信息
git push origin master 推送master分支
git push origin dev 推送dev分支

/**master分支是主分支，因此要时刻与远程同步；
dev分支是开发分支，团队所有成员都需要在上面工作，所以也需要与远程同步；
bug分支只用于在本地修复bug，就没必要推到远程了，除非老板要看看你每周到底修复了几个bug；
feature分支是否推到远程，取决于你是否和你的小伙伴合作在上面开发。**/

git tag v1.0  添加标签
git tag 查看所有标签
git tag v0.8 4ff353da  给提交过的id加标签
git tag -a v0.1 -m "version 0.1 released" 3628164  -a指定标签名  -m指定说明文字
git show v1.0 显示v1.0的说明文字
git tag -s v0.2 -m "signed version 0.2 released" fec145a   通过-s用私钥签名一个标签
  /**签名采用PGP签名，因此，必须首先安装gpg（GnuPG），如果没有找到gpg，或者没有gpg密钥对，就会报错：**/
git tag -d v1.0 删除标签
git push origin v1.0 推送远程标签
git push origin --tags 推送全部标签
删除标签.先本地.后远程 本地| git tag -d v1.0  远程| git push origin :refs/tags/v1.0
git config --global alias.st status  用st代替status
--global参数是全局参数，也就是这些命令在这台电脑的所有Git仓库下都有用。










