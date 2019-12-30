# git

## 1、git是什么东西，到底有什么用
 - 就是一个历史版本控制系统(保存代码信息)
## 版本控制系统的分类：
    - svn：集中式
    - git：分布式
## linux 的常用命令
    + cd 文件名：打开当前文件
    + mkdir 文件名：创建一个文件夹
    + cd ../ : 返回上一级目录
    + cd /: 返回根目录
    + cls：清屏

## git的使用
- 1、git的工作原理
    + 工作区：就是你写代码的地方
    + 暂存区：临时存储代码的地方
    + 历史区：生成历史版本的地方

- 2、git的全局配置
    + git config -l(查看全局配置)
    + git config --global user.name 'xxx'
    + git config --global user.email 'xxxx'

- 3、创建本地仓库，完成版本控制
    - 1、创建本地仓库
        + git init：初始化git仓库(会默认出现.git文件，他是git仓库的信息文件，不能删除)
    - 2、在本地工作区编辑完成代码之后，把代码提交到暂存区
        + git add . : 把工作区的所有修改的文件提交到暂存区
        + git add -A: 把工作区的所有修改的文件提交到暂存区
        + git add 文件名：把工作区指定的文件提交到暂存区
        + git status:查看文件提交状态(如果是红色的，就是在工作区，绿色的在暂存区，如果显示 working tree clean，说明文件已经提交到历史区)
        + clear：清屏

    - 3、把暂存区的代码提交到历史区
        + git commit -m'注释' ：把暂存区的文件提交到历史区(字符串里写的是当前提交的描述信息)
        + git log:查看历史版本信息
        + git reflog:查看所有的历史版本信息
        + git reset --hard 历史版本号：把指定版本的代码回滚到本地

- 4、介绍远程仓库github
        + github是一个开源的代码分享平台；每一个github账户都可以把自己的代码分享到这个平台上，那他就是充当中央服务器的角色，把代码提交到这个平台上之后，你可以在任何一个有网络的地方去下载代码，当然了，谁有下载的权限是有你来配置的
        1、在头像下的Settings
            + Profile：设置昵称、公开的邮箱、简介、头像
            + account：设置用户名（登录名）、
            + security：修改密码

        2、创建仓库
            + new repository
                + publice：创建一个开源的仓库
                + peivate：私有仓库作为团队内部开发
            + 填写信息
            + create repository
            + 仓库的settings
                + delete this repository（删除库）
                + Collaborators 设置仓库的管理者

- 5、把本地的代码提交到远程仓库
    + git remote -v(查看本地仓库和远程仓库的连接状态)
    + git remote add origin 远程仓库项目地址：把本地仓库和指定的远程仓库项目进行关联(origin可以起别的名字，但是一般大家都叫origin)
    + git remote rm origin: 解除本地和远程仓库的关联

    + git pull origin master:把远程仓库的代码拉取到本地
    + git push origin master：把本地的代码推送到远程仓库

    + git clone 远程仓库项目地址 本地的项目名(git init  git remote add  git pull)
    + 一般在真正的项目中，你们的项目老大去构建项目的框架，然后上传到远程仓库，之后每一个小组成员都去拉取这个项目到自己的本地去开发
    