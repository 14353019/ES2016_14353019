安装git和建安装git和建立新的仓库：
（1）输入sudo apt-get install git，在虚拟机上安装git；
（2）输入mkdir learngit，建立仓库，输入cd learngit，进入仓库中；
（3）输入pwd，显示当前目录；
（4）输入git init表明当前目录是可以被管理的仓库；
（5）利用输入git add README.md，将文件添加到仓库；
（6）输入git commit -m "wrote a readme file，将文件提交到仓库中；
添加远程库：
（1）登陆github的网站，注册账户，新建一个远程的仓库；
（2）输入git remote add ES2016_14353019 git@https://github.com/14353019/ES2016_14353019.git,建立本地仓库和远程仓库的连接；
（3）输入git push -u origin master，将本地仓库地文件上传到远程仓库中；
