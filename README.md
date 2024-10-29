# Git
主要介绍了常见的Git命令，小白专用
## 一、常用命令
- **配置用户名和邮箱**
  - 设置全局用户名
    ```bash
    git config --global user.name "your name"
    ```
  - 设置全局邮箱
    ```bash
    git config --global user.email "your email"
    ```

- **克隆仓库到本地**
  - 克隆远程仓库到本地，此时本地与远程仓库已建立链接，远程仓库被标识为 `origin`
    ```bash
    git clone https://github.com/yourname/yourproject.git
    ```

- **创建新分支,此举是为了保持代码整洁，不污染主分支（可选）**
  - 创建并切换到新分支
    ```bash
    git checkout -b newbranch
    ```

- **修改文件后提交到暂存区**
  - 将所有修改的文件添加到暂存区
    ```bash
    git add .
    ```
  - 提交暂存区的更改到本地仓库，并添加提交信息
    ```bash
    git commit -m "your message"
    ```
  - 推送合并后的更改到你的远程仓库，如果创建了新分支，则使用新分支名
    ```bash
    git push origin 分支名
    ```
- **（附加步骤）添加原作者仓库**
  - 添加原作者仓库，被标识为 `upstream`，确保你 fork 的仓库可以获取最新代码
    ```bash
    git remote add upstream https://github.com/原始用户名/仓库名.git
    ```
  - 获取上游仓库更新
    ```bash
    git fetch upstream
    ```
  - 合并上游更新到本地主分支（假设主分支名为 `main`）
    ```bash
    git checkout main
    git merge upstream/main
    ```
  - 推送合并后的更改到你的远程仓库，如果创建了新分支，则使用新分支名
    ```bash
    git push origin 分支名
    ```
