# GIT 常用命令

$ git init   将当前文件夹用git仓库管理起来<br>
$ git add .  将所有改动提交到工作缓存区<br>
$ git status  查看提交状态<br>
$ git commit -m "注释"    将工作缓存区提交到仓库<br>
$ git remote add origin repository提交到远程仓库后面是仓库创建仓库产生的链接<br>
$ git push -u origin master   更新远程代码

## 版本回退
$ git reset --hard commit_id 版本回退<br>
$ git log 可以查看提交历史，回退前用以便确定要回退到哪个版本。<br>
$ git reflog 要重返未来，用查看命令历史以便确定要回到未来的哪个版本。<br>

## 创建与合并分支

$ git branch 查看分支<br>
$ git branch name 创建分支<br>
$ git checkout name 切换分支<br>
$ git checkout -b name 创建+切换分支<br>
$ git merge name 合并某分支到当前分支<br>
$ git branch -d name 删除分支<br>

##git使用ssh密钥
1.查看本地是否有密钥对，如果存在就删除<br>
    cd ~/.ssh<br>
    id_dsa id_dsa.pub<br>
2.重新生成密钥对然后一直回车<br>
    ssh-keygen -t rsa -C "your_email@youremail.com"<br>
3.查看本地生成的密钥<br>
    cat ~/.ssh/id_rsa.pub<br>
4.登陆你的github帐户。然后 Account Settings -> 左栏点击 SSH Keys -> 点击 Add SSH key<br>
5.然后你复制上面的公钥内容，粘贴进“Key”文本域内。 title域，你随便填一个都行。
