Github �����̳�
���� ��̼���
http://www.runoob.com/w3cnote/git-guide.html


http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013743256916071d599b3aed534aaab22a0db6c4e07fd0000
http://www.ruanyifeng.com/blog/2014/06/git_remote.html

https://github.com/michaelliao/learngit/blob/master/Git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/git%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0.md


http://blog.csdn.net/u013215018/article/details/53613457


Git��������
http://www.cnblogs.com/sysu-blackbear/p/3463475.html

�������ã�
1. ��װ��ÿ�������������Ա����ţ�������ֺ�Email��ַ
$ git config --global user.name "Your Name" 
$ git config --global user.email "email@example.com"
ssh-keygen -t rsa -C "YOUR EMAIL"

Permission denied (publickey).
fatal: Could not read from remote repository.
Please make sure you have the correct access rights
and the repository exists.

���������������Ϊ��û����github�˺����SSH key

2.��ʼ��һ������Git�ֿ⣬ʹ��git init���touch README.md�������������һ���ļ��� git pull origin master


3.����ļ���Git�ֿ⣬��������

    ��һ����ʹ������git add <file>��ע�⣬�ɷ������ʹ�ã���Ӷ���ļ���

    �ڶ�����ʹ������git commit����ɡ�

4. ��ӵ�Զ�̿⣨github��

    ��1����github�ϴ���һ����Ϊswjsrc�Ŀղֿ�
    
    ��2�����Զ�ֿ̲�
    $ git remote add swjgh https://github.com/swjgithub/swjsrc
��$ git remote add origin https://github.com/swjgithub/swjsrc
    
    (3)�ѱ����������͵�githubԶ�̿���(��һ��push ������ -u ����Զ�ֿ̲�)

    $ git push -u origin master


git pull --rebase origin master


����������

��1��������SSH Key�����û���Ŀ¼�£�������û��.sshĿ¼������У��ٿ������Ŀ¼����û��id_rsa��id_rsa.pub�������ļ�������Ѿ����ˣ���ֱ��������һ�������û�У���Shell��Windows�´�Git Bash��������SSH Key��

$ ssh-keygen -t rsa -C "youremail@example.com"

��2������½GitHub���򿪡�Account settings������SSH Keys��ҳ�棺

Ȼ�󣬵㡰Add SSH Key������������Title����Key�ı�����ճ��id_rsa.pub�ļ������ݣ�

5.�ϴ�������
git remote��git clone

///////////////////////////
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/zxdong262/paper-slider.git
git push -u origin master


$ ssh -T git@github.com




