Git总结
====
### 设置用户信息
git config --global user.name "用户名"   //设置用户名  
git config --global user.email "用户邮箱"   //设置邮箱  
git config --global user.name    //查看用户名是否配置成功  
git config --global user.email    //查看邮箱是否配置  

### 创建本地仓库
git init 仓库名   //创建一个新的带Git仓库的项目  
git init   //为已存在的项目生成一个Git仓库

### 添加文件到暂存区
git add 文件名   //将工作区的某个文件添加到暂存区     
git add -u   //添加所有被tracked文件中被修改或删除的文件信息到暂存区，不处理untracked的文件  
git add -A   //添加所有被tracked文件中被修改或删除的文件信息到暂存区，包括untracked的文件  
git add .   //将当前工作区的所有文件都加入暂存区  
git add -i   //进入交互界面模式，按需添加文件到缓存区

### 将暂存区内容添加到本地仓库
git commit -m "提交说明"

### 查看工作区与缓存区状态
git status

### 推送本地仓库到远程仓库
git remote add origin 远程仓库地址   
接着把本地仓库推送到远程仓库，这里的 -u参数 作为第一次提交使用，
作用是把本地master分支和远程master分支关联起来  
git push -u origin master

### 修改远程仓库地址
git remote set-url origin 远程仓库地址  
也可以先删除origin后再添加  
git remote rm origin    //删除仓库关联  
git remote add origin 远程仓库地址    //添加仓库关联
