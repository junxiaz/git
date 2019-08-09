# git使用说明
## git说明：
git:分布式版本控制工具
![Git工作流程](https://github.com/junxiaz/git/blob/master/imgs/Git_workflow.png)

## git安装：
1. msysgit.github.io
2. Use git from git bash only..,（其他默认下一步）
3. 配置path： （例）E:\program\Git\bin
4. 配置git：用户名和邮箱
5. 右键 Git Bash Here
6. git config --global user.name 'junxiaz'
7. git config --global user.email 'junxiaz@163.com'
8. 查看.gitconfig：C:\Users\Administrator\.gitconfig
9. 搭建git服务器（远程仓库）：统一的托管网站（https://github.com/）
10. 免秘钥登录方法：配置ssh
	1. ssh：本地--远程
    2. 配置ssh：先在本地配置，发送给远程
    3. 先在C:\Users\Administrator本地生成ssh：ssh-keygen -t rsa -C junxiaz@163.com（其他回车）
    4. 发送给远程：github => settings => SSH and ... => New SSH  => （title随意、key输入在本地生成的ssh：将本地生成的id_rsa.pub内同复制到key中）
    5. 测试连通性：ssh -T git@github.com（若本地与远程成功通信，则可以在/.ssh目录中发现know_hosts文件，若失败多尝试几次、检查回车符）

## git与github项目进行关联
1. repositories => new => 建立项目 => 生成https://github.com/junxiaz/git.git
2. 将本地项目与远程项目关联：git remote add origin git@github.com:junxiaz/git.git

## 第一次发布项目（本地-远程）
1. git add . //工作区文件 => 暂存区
2. git commit -m '注释内容' //暂存区文件 => 工作区本地分支（默认master）
3. git push -u origin master

## 第一次下载项目（远程-本地）
1. git clone git@github.com:junxiaz/git.git

## 提交（本地-远程）
（在当前工作目录，右键Git Bash Here）
1. git add .
2. git commit -m '提交到分支'
3. git push origin master

## 更新项目（远程-本地）
git pull

## 在编辑器中操作git（例如Eclipse）
`目前的eclipse基本都支持git，若不支持则在eclipse marktplace搜git安装配置`
1. team-git-configuration -邮箱 用户名
2. general -network -ssh2选中 生成的ssh目录

### 第一次发布
1. share project
2. add to index：加入到暂存区
3. commit：提交到本地分支
4. 将项目推送到远程：右键 => team => remote => push ===

### 提交
1. team-add to index
2. team -commit
3. team -push

### commit方式
commit and push 或 commit按钮的区别：
1. commit按钮：不能单独的push某一个文件，只能push整个项目
2. commit and push：可以单独push某一个文件

### 第一次下载
import -clone -输入 https/ssh的唯一标识符

### 更新
team - remote - pull

## git冲突的解决
1. 发现冲突：进入同步视图 右键 => team => synchronized...
2. 解决冲突：
	1. add to index:添加到本地暂存区
    2. commit:提交到本地分支
    3. pull:更新服务端的分支内容到本地分支
    4. 修改冲突：直接修改或者merge tool（--->已经变为了普通本地文件）,add to index,commit push

## git多人团队开发
1. GitHub该项目中 => settings
2. 增加合作者：collaboration中加入合作者：GitHub全名或邮箱 => 发送邀请链接
3. 合作者： 打开该链接接受邀请：合作开发...clone项目 => 修改 => add\commit\push

## git常用命令说明：
![Git命令](https://github.com/junxiaz/git/blob/master/imgs/Git_articlex.jpg)
1. 在本地新建git项目，在项目根目录中右键 Git Bash Here
2. git init:新建git项目
3. git add:将本地文件增加到暂存区
4. git commit:将暂存区的文件提交到本地仓库（本地仓库，默认master分支）
5. git push:将本地仓库的文件推送到远程仓库（远程分支）
