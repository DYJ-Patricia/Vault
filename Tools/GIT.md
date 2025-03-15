# Git 与 Git Bash 常用用法


## Git 基本用法

### 初始化仓库

* `git init`：在当前目录初始化一个新的 Git 仓库。

### 添加文件到暂存区

* `git add <文件名>`：添加指定文件到暂存区。
* `git add .`：添加所有更改的文件到暂存区。
* `git add *.txt`


### 提交更改

* `git commit -m "提交信息"`：提交暂存区的更改到本地仓库。
    * `-m`：指定提交信息。
* `git commit`:VIM交互。

### 查看仓库状态

* `git status`：查看当前仓库的状态，包括已修改、已暂存、未跟踪的文件。

### 查看提交历史

* `git log`：查看提交历史。
* `git log --oneline`：以简洁的方式查看提交历史。

### 创建分支

* `git branch <分支名>`：创建新的分支。

### 切换分支

* `git checkout <分支名>`：切换到指定分支。
* `git checkout -b <分支名>`：创建并切换到新的分支。

### 合并分支

* `git merge <分支名>`：将指定分支的更改合并到当前分支。

### 删除分支

* `git branch -d <分支名>`：删除指定分支（已合并）。
* `git branch -D <分支名>`：强制删除指定分支（未合并）。

### 添加远程仓库

* `git remote add origin <远程仓库URL>`：添加远程仓库。
    * `origin`：远程仓库的别名。

### 推送更改到远程仓库

* `git push origin <分支名>`：推送本地分支的更改到远程仓库。
* `git push -u origin <分支名>`：首次推送时设置上游分支。

### 从远程仓库拉取更改

* `git pull origin <分支名>`：拉取远程分支的更改并合并到本地分支。

### 克隆远程仓库

* `git clone <远程仓库URL>`：克隆远程仓库到本地。

### 查看远程仓库信息

* `git remote -v`：查看远程仓库的详细信息。

### 查看差异
- `git diff`:显示工作目录中未暂存的更改。
- `git diff HEAD`:查看工作区和HEAD的差异。
- `git diff --cached`:查看暂存区和HEAD的差异。
- `git diff <ID> <ID>`:两个版本之间的差异。
- `git diff <ID> <ID> <文件名>`:只查看这个文件的差异。


### 解决冲突

* 手动编辑冲突文件，解决冲突。
* `git add <冲突文件>`：标记冲突文件为已解决。
* `git commit -m "解决冲突"`：提交解决冲突后的更改。

### 撤销更改

* `git checkout -- <文件名>`：撤销工作区的更改。
* `git reset HEAD <文件名>`：撤销暂存区的更改。
* `git reset HEAD^`:回退到上一个版本。
* `git reset --hard <commit ID>`：回退到指定提交。

### 手动添加忽略文件
- `touch .gitignore`:创建忽略文件。
- `echo "*.exe" >> .gitignore`：省略上传所有.exe文件

### Obsidian的github备份
#### .gitignore中写入：
- echo ".obsidian/plugins/github-sync/main.js" >> .gitignore
- echo ".obsidian/plugins/github-sync/manifest.json" >> .gitignore
- echo ".obsidian/plugins/github-sync/styles.css" >> .gitignore
- echo ".obsidian/plugins/github-sync/data.json" >> .gitignore

## Git Bash 常用命令

### 导航

* `cd <目录>`：切换目录。
* `cd ..`：返回上一级目录。
* `ls`：列出当前目录的文件和目录。
* `pwd`：显示当前目录的路径。

### 文件操作

* `touch <文件名>`：创建空文件。
* `mkdir <目录名>`：创建目录。
* `rm <文件名>`：删除文件。
* `rm -r <目录名>`：删除目录及其内容。
* `cat <文件名>`:观看文件内容。
* `echo "content" > <文件名>`:覆盖写入内容，没有文件就自动创建。
* `echo "content" >> <文件名>`:接后文写入内容。
* `vim <文件名>`:打开vim编辑器编辑文件。[具体操作](VIM)。


### 其他

* `clear`：清空终端屏幕。
* `history`：查看命令历史记录。

## 常用 Git 配置

### 设置用户名和邮箱

* `git config --global user.name "你的用户名"`
* `git config --global user.email "你的邮箱"`

### 设置默认文本编辑器

* `git config --global core.editor "编辑器路径"`



## 参考资料

* [Git 官方文档](https://git-scm.com/doc)
* [Pro Git](https://git-scm.com/book/zh/v2)



