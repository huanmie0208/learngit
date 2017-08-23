Git is a distributed version control system.
Git is 免费的 software.
我是zhongguoren
中国人

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




