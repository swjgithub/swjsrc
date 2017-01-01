Github 简明教程
分类 编程技术
http://www.runoob.com/w3cnote/git-guide.html


一、环境配置：
1. 安装后每个机器都必须自报家门：你的名字和Email地址
    $ git config --global user.name "Your Name" 
    $ git config --global user.email "email@example.com"
    查看配置信息 git config --list

2.ssh授权
   （1）首先在本地创建ssh key；
       ssh-keygen -t rsa -C "YOUR EMAIL"
   （2）到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title随便填，粘贴在你电脑上生成的key。
   （3）测试
      $ ssh -T git@github.com
      见到以下信息为成功：
      Hi swjgithub! You've successfully authenticated, but GitHub does not provide shell access.

3.创建目录或使用我们指定目录作为Git仓库,主获取远程主要文件

    （1）建立并进入目录 
      mkdir src
      cd swjsrc
    （2）初始化本地Git仓库
     git init [swjsrc]
     初始化一个本地Git仓库，使用git init命令。
    （3）获取README.md文件
      touch README.md。这命令是添加一个文件。 
      或git pull origin master

      或git pull --rebase origin master

4.添加文件到本地Git仓库，分两步：

     第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；
     第二步，使用命令git commit，完成。

5. 添加到远程库（github）
    （1）在github上创建一个名为swjsrc的空仓库    
    （2）添加远程仓库
     $ git remote add origin git@github.com:swjgithub/swjsrc.git
     测试
    
    (3)把本地内容推送到github远程库上(第一次push 参数带 -u 关联远程仓库)

     $ git push -u origin master



【问题解决】
Permission denied (publickey).
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.

出现这个问题是因为，没有在github账号添加SSH key


【问题解决】

$ git push -u origin master
To github.com:swjgithub/swjsrc.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:swjgithub/swjsrc.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

###################################################
是用 -f 参数 来push: 
git push -f origin master
#####################################################
资料来源于http://stackoverflow.com/

【问题解决】

第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

$ ssh-keygen -t rsa -C "youremail@example.com"

第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面：

然后，点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容：

5.上传和下载
git remote和git clone

///////////////////////////
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/zxdong262/paper-slider.git
git push -u origin master


$ ssh -T git@github.com


######################


http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000
http://www.ruanyifeng.com/blog/2014/06/git_remote.html

https://github.com/michaelliao/learngit/blob/master/Git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0.md


http://blog.csdn.net/u013215018/article/details/53613457


Git常用命令
http://www.cnblogs.com/sysu-blackbear/p/3463475.html

