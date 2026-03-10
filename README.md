## 一、提交代码（基本操作）
### 1. 初始化仓库
```bash
git init  # 初始化一个 Git 仓库，文件夹中会生成一个 .git 文件夹
```

### 2. 查看未提交的文件
```bash
git status  # 查看当前仓库的状态
```

### 3. 添加远程仓库
```bash
git remote add origin <url>  # 添加远程仓库，<url> 是远程仓库的 URL
```

### 4. 添加文件到仓库
```bash
git add <file>   # 添加特定文件
git add .        # 添加所有文件
git add --all    # 添加所有文件并提交到当前分支
```

### 5. 提交文件到仓库
```bash
git commit -m "commit message"  # 提交当前分支的所有变更到本地仓库，<commit message> 是提交信息
```

### 6. 推送本地分支到远程仓库
```bash
git push -u origin <branch>  # 推送当前分支到远程仓库，<branch> 是远程分支的名称，常见的分支有 main、master 等
```

## 二、分支操作
### 1. 查看当前分支
```bash
git branch
```

### 2. 切换分支
```bash
git checkout <branch>
```

### 3. 创建新分支
```bash
git branch -c <branch>
```

### 4. 合并分支
```bash
git merge <branch>  # 合并指定分支到当前分支
git merge --no-ff <branch>  # 合并指定分支到当前分支，不使用快进合并
git merge --abort  # 取消合并操作
```

### 5. 查看合并冲突
```bash
git diff
```

## 三、返回提交状态
### 1. 查看提交历史
```bash
git log  # 查看所有提交历史
git log --oneline  # 查看所有提交历史，每条提交显示一行
git reflog  # 查看所有提交历史，包括回滚操作
```

### 2. 回滚提交（丢失未提交的变更）
```bash
git reset --hard HEAD^  # 回滚到上一个提交，所有未提交的变更会被丢失
git reset --hard HEAD~100  # 回滚到上 100 个提交
git reset --hard <commit-id>  # 回滚到指定提交
```

### 3. 回滚提交（保留未提交的变更）
```bash
git reset --soft HEAD^  # 回滚到上一个提交，保留未提交的变更
git reset --soft HEAD~100  # 回滚到上 100 个提交
git reset --soft <commit-id>  # 回滚到指定提交
```

## 四、clone （克隆仓库）
```bash
git clone <url>  # 克隆远程仓库到本地，<url> 是远程仓库的 URL
```

例如：
```bash
git clone https://github.com/harvest0623/Parent-child-education.git
```