#git全局配置  
git config --global user.name="gongbing"  
git config --global user.email="834718027@qq.com"  
#ssh秘钥生成  
ssh-keygen -t rsa -C "834718027@qq.com"  

#初始化仓库  
git init  

#丢弃修改  
git checkout --file  #把文件恢复到上个版本状态

#提交到暂存区  
git add filename  
git add .  
#撤销修改  
git reset HEAD -- file #file 是你提交的文件名

#提交到版本库  
git commit -m "描述信息"  
#版本回退  
git reset --hard HEAD^  
git reset --hard [id] #id表是提交版本id  

#查看状态  
git status  

#查看修改内容  
git diff  
git diff HEAD -- readme.txt #查看工作区和版本库的差别

#查看提交日志  
#方括号内容可选
git log [--pretty=oneline]  [--abbrev-commit]  
git reflog  	

#从版本库中删除文件  
git rm file
git commit -m "提交信息"  

#添加远程库
git remote add origin git@github.com:gongbing123/git.git  
#查看  
git remote  
git remote -v  
#删除  
git remote remove origin  

#拉取  
git pull origin master  
#推送  
git push [-u] origin master  
#克隆  
git clone git@github.com:gongbing123/git.git  

#创建切换分支  
git checkout -b dev  
#查看分支  
git branch  
#合并分支  
git merge [--no-ff -m "描述信息"] dev  #--no-ff 参数表示禁用 fast foward  
#删除分支  
git branch -d dev  #-D 强行删除  

#储藏工作  
git stash  
#查看  
git stash list  
#恢复
git stash apply
git stash pop #恢复的同时删除  

#复制特定提交到当前分支  
git cherry-pick commit_id  

#将push 提交的分叉整理成直线  
git rebase  

#打标签  
git tag [v0.1] [id]  
#查看标签  
git tag  
#查看标签详细信息  
git show v0.1  

