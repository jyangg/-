# -
学习博客：http://www.ityouknow.com/

git 
git简单使用手册

Git clone  +地址   拉远程代码到本地
git branch <name>   创建分支
Git branch -a  查看本地分支
git branch -d <BranchName> 删除本地某分支
git checkout -b jyangg origin/jyangg  创建本地分支
Git pull    拉远程分支代码 ============提交步骤
Git add  要修改的代码
Git commit 提交到本地代码
Git commit -m ‘’ 提交到本地代码 并加上注释
Git push orgin develop 上传代码到远程分支
Git status  查看状态，可以看到修改状态
Git log 查看操作日志
Git checkout + 分支名   切换分支
git checkout +文件    撤销
git merge yangjun   //把yangjun分支合并到当前分支



git  rebase  develop  //用rebase合并主干的修改，如果有冲突在此时解决
git reset --hard commit_id   撤销本地commit 但是未push的
=============================================================
1. 拉取代码
gerrit里面获取clone命令

例如：
git
git clone ssh://wu_xx@wirelesscode.ctripcorp.com:29418/Wireless/RN_Product
2. 更新代码
git pull //直接更新代码
git pull –-prune //更新代码, 新分支信息会同步到本地, 新版本，创建新分支之后需要
3. 创建本地分支
比如在本地创建rel/7.7， 对应远端的rel/7.7分支

git checkout -b rel/7.7 origin/7.7
4. 提交代码
务必遵守流程： 更新代码-处理冲突-提交代码

更新代码
git pull
发现冲突

本地stash已经修改过的内容
git stash
重新更新最新代码

git pull --rebase
还原本地stash的代码

git stash pop
如果有冲突文件，处理冲突文件
添加需要提交的文件

git add file_a file_b file_c
添加提交注释
git commit -m "本次提交说明"
push本次提交到gerrit，rel/7.7为远端仓库名
git push origin HEAD:refs/for/rel/7.7
5. 其它几个常用命令
分支合并，比如本地分支issueFix， 合并到rel/7.7
git checkout rel/7.7
git merge issueFix
还原到某个点

查看commitid

git log
还原到某个commitid

git reset --hard _comit_id_xxxxx
放弃git add, 但是未commit的文件
git checkout file_a file_b file_c

===============================

删除分支：git branch -d <name>


------------------------------------------------------------------------------
idea

shift +F6  重命名
Ctrl+ Y  删除一行
Ctrl+Alt+L，格式化代码
Ctrl+F12  查看文件结构
alt +insert  getset自动生成,生成set方法
sout  打印
代码提示 alt +/
Ctrl+alt+B 或Ctrl+alt+鼠标点击 查看接口实现
ctr+shift+u 大小写
Ctrl+Alt+L  
Ctrl+R 当前文件替换
Ctrl+ shift+ F 全文搜索
Ctrl+ F   当前文件搜索
shift+shift 搜索
Ctrl+shift+n 搜索
Ctrl+ alt + V  new一个对象
Ctrl＋Alt＋T可以把代码包在一块内，例如try/catch
Ctrl +N
Ctrl+shift+N 
2个shift
alt+f8 查看断点值
f7跳入
f8 下一步
shift+f8 跳出
Ctrl+G  跳转到指定行号
优化导入（Code | Optimize Imports）（Ctrl+Alt+O）
