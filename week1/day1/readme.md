### 常用linux命名
cd 进入文件夹
cd .. 返回到上级目录
ls
ls -al 查看所有的目录（包含隐藏的文件）
mkdir 文件夹名  新建文件夹
touch  文件名   新建文件
vi 1.txt  编辑文件
 - 按i键进入编辑状态
 - 编辑完后按esc键退出编辑  按：键->:wq 保存退出 :q不保存退出 :q！强制退出  然后按回车键
cat 1.txt  查看文件
rm -rf 文件名  删除
pwd 查看路径


### 配置git  提交远程服务器github
先去github注册用户名和密码
https://github.com
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
git config --list 看下是否配置成功

git config credential.helper ''  清除用户配置的信息

### git使用
git status  查看提交的状态
- 由工作区提交到暂存区
git add .
- 由暂存区提交到历史区
git commit -m"对添加内容的说明"

### 本地仓库和远程仓库关联
- 关联 git remote add zf https://github.com/zfpx/testGit.git
- 查看关联的远程仓库  git remote -v
- 移除关联远程仓库 git remote remove zf
- 把本地仓库内容提交到远程仓库 git push zf master

### 处理本地仓库跟远程仓库不相同的情况
- git pull zf master  先更新（把远程仓库内容拉取到本地仓库）
> 第一次拉取时，若拉取不下来 加个参数 如下：
> git pull zf master --allow-unrelated-histories
- 例如要提交本地仓库的c.txt
- git add .
- git commit -m"c"
- git push zf master

### 克隆远程仓库
git clone https://github.com/zfpx/testGit.git
>相当于做了两件事，1.创建了本地仓库testGit 2.让本地仓库和远程仓库关联起来

1.第一次克隆远程仓库
2.每天执行git pull origin master 更新讲义

## 提交作业
- 先以你的github账号登录，然后把老师的git仓库地址复制到地址栏按回车
- 点fork按钮 (把老师的仓库克隆到你的远程仓库)
- 把自己远程仓库克隆到本地 （自己是可以向自己的远程仓库提交内容）
    git clone 克隆的远程仓库地址
- 把作业提交到自己的远程仓库（远程仓库：指从老师那边克隆的仓库）
    git add . git commit -m"" git push origin master
- 点击new pull request 按钮 -> 点击create pull request  (向老师的仓库发起合并的请求)




















