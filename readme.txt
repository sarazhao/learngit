git is a version control system.
git is free software.

git init 初始化一个git repository
git add <file>  添加文件，可以多次使用，也可以一次添加多个，空格隔开
git commit 提交。-m 参数跟说明

git status 查看git工作区的状态
git diff <file>  查看文件修改内容

git reset --hard commit_id git可以在版本历史中穿梭
HEAD指向当前版本
HEAD^上一个版本
HEAD^^上两个版本
HEAD~100上100个版本
git log 查看提交历史回到历史版本，参数--pretty=oneline可以使输出更简洁
git reflog 查看命令历史重返未来版本


场景1：当你改乱了工作区某文件，想丢弃修改时用命令git checkout -- file
场景2：当你不但改乱了工作区的某文件，还添加到了暂存区时，想要丢弃修改分两步
       第一步用命令git reset HEAD file
	   第二步跟场景1类似，用命令git checkout -- file
场景3：已经提交了不合适的修改到版本库时，想要撤销，要先
        git log --pretty=oneline  找到版本ID
		然后git reset --hard commit_id 回退到版本
		但是这样操作的前提是修改还没有推送到远程库
		
		
git rm test.txt  删除test.txt
git commit -m "cccc"  提交到版本库，并添加备注信息cccc

