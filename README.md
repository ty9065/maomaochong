# maomaochong

This is my first github project!

## 学习笔记一：
![git图解](http://img.blog.csdn.net/20170422114557808?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvanRyYWN5ZHk=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center "git图解")
#### git命令行——本地修改的文件提交到github远程仓库上：  
1. 进入本地仓库，查看状态：`git status`，被修改的文件标为红色;  
2. 提交修改后的文件到本地缓存区：`git add README.md`，成功后再次查看状态时，被修改的文件被标为绿色;  
注：`git add .` 　   ----添加所有新增的文件  
　　`git commit .` ----提交所有新增的文件到暂存区  
3. 提交更新后的文件，并添加备注说明：`git commit -m "提交说明"`  
4. 将本地仓库修改后的文件push到远程仓库：`git push`  

#### mac下复制SSH到公有key:  
`pbcopy < ~/.ssh/id_rsa.pub`

#### github提交更新没有绿格:  
原因：本地git的配置邮箱和github上面的邮箱不一致  
查看本地邮箱：mac bash下输入`git config user.email`，不显示或不一致则需要配置  
配置本地邮箱：mac bash下输入`git config --global user.email "邮箱名"`

---

## 学习笔记二：  
#### mac bash进入python shell:  
mac bash下输入`python`后回车就是python shell界面了，且会显示python版本(2.7.10)；  
退出该界面回到 mac bash按`ctrl+d`即可。 

#### 判断pip是否已安装：  
mac bash下输入`pip --version`，如果结果显示版本号，即为已安装。  
另，pip is already installed if you are using Python 2 >=2.7.9 or Python 3 >=3.4  

---------

### virtualenv（虚拟环境）:  
创建**独立**的python开发环境，可以解决版本冲突及权限等问题；  
例如，A项目使用python2.7, 而B项目使用python3.3时，使用virtualenv可以做到互不干扰。  
#### 判断virtualenv是否已安装：  
mac bash下输入`virtualenv --version`，如果结果显示版本号，即为已安装。  
#### mac下virtualenv的安装方法：  
mac bash下输入`sudo easy_install virtualenv`，回车后等待安装完成。  
#### 使用virtualenv创建虚拟环境时会自动安装pip  
* 创建虚拟环境：`virtualenv venv`  
* 激活虚拟环境：`source venv/bin/activate`   
* 退出虚拟环境：`deactivate`   

--------

### flask（框架）：  
#### 虚拟环境中安装flask：  
`pip install flask`  
#### 判断flask是否安装成功：  
启动python解释器，能够导入flask即安装成功：  
`python`  
`>>>import flask`
    
