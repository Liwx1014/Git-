# Git
主要介绍了常见的Git命令，小白专用
## 一、常用命令
1.Linux 配置用户名和邮箱
git config --global user.name "your name"
git config --global user.email "your email"
git config --global user.email "
git config --global user.name "your name"
## 1.克隆仓库到本地 ,这个时候仓库已经存在本地和远程已经建立链接 https://github.com/yourname/yourproject.git 被标识为origin
git clone https://github.com/yourname/yourproject.git
## 2.创建新分支（可选）
git checkout -b newbranch
## 3.修改文件后提交到暂存区
git add .
git commit -m "your message"
## （附加步骤）4.添加原作者仓库 https://github.com/原始用户名/仓库名.git 被标识为upstream，保证你fork的仓库获取最新代码
git remote add upstream https://github.com/原始用户名/仓库名.git
git fetch upstream   #更新
git checkout main   #取决于原仓库的分支名
git merge  upstream/main
git push origin main


