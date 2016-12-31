
http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000
http://www.ruanyifeng.com/blog/2014/06/git_remote.html

https://github.com/michaelliao/learngit/blob/master/Git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0.md


http://blog.csdn.net/u013215018/article/details/53613457


Git常用命令
http://www.cnblogs.com/sysu-blackbear/p/3463475.html

环境配置：
1. 安装后每个机器都必须自报家门：你的名字和Email地址
$ git config --global user.name "Your Name" 
$ git config --global user.email "email@example.com"
ssh-keygen -t rsa -C "YOUR EMAIL"

Permission denied (publickey).
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.

出现这个问题是因为，没有在github账号添加SSH key

2.初始化一个本地Git仓库，使用git init命令。touch README.md。这命令是添加一个文件。 git pull origin master


3.添加文件到Git仓库，分两步：

    第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；

    第二步，使用命令git commit，完成。

4. 添加到远程库（github）

    （1）在github上创建一个名为swjsrc的空仓库
    
    （2）添加远程仓库
    $ git remote add swjgh https://github.com/swjgithub/swjsrc
或$ git remote add origin https://github.com/swjgithub/swjsrc
    
    (3)把本地内容推送到github远程库上(第一次push 参数带 -u 关联远程仓库)

    $ git push -u origin master


git pull --rebase origin master


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




