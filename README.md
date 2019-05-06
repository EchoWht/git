##  一.项目提交
1. 先拉取最新的内容
git pull
2. 添加当前新增或修改的文件
git add 某个文件名
3. 提交
git commit -m""
4. 把本地最新的推到master分支上 
git push -u origin master


##  二.合并分支

1. 切换到主分支
git checkout master

2. 拉取master分支上最新的资源
git pull

3. 本地合并（wht是分支名）
git merge wht

4. 把本地最新的推到master分支上 
git push -u origin master


##  三.本地文件已修改，需要强制pull

git fetch --all  
git reset --hard origin/master 
git pull

## 四.git 因文件权限修改导致都显示modify
    git config core.fileMode false
## 五.git 恢复本地误删的文件(例如误删了themes下的default 文件夹)
    1. git reset HEAD themes/default
    2. git checkout themes/default
## 六.git 误提交大量文件，版本恢复
    1. git reset --hard c29afeaa1f7434eac8f8e56227ce5910d38f2267
    2. git push -f -u origin master
    3. 其他协同同事更新  git pull origin master
    
## 查询
    1.  查询某个关键词
    git log --grep=word
    2.  查询某个提交人的关键词
    git log --author echowht --grep=word
    3.  查询某个文件每一行最后操作的用户，并且导出到具体文件
    git blame xxx.c >blame.log
    
## 导出
    1. 导出某个提交人的commit log(导出结果在项目的根目录)
    git log --author echowht log.txt
  
## emoji含义（github，code.aliyun.com ,coding未测试）
-  🎨 - 改进结构和代码格式
-  ⚡️ - 优化性能
-  🔥 - 移除代码或文件
-  🐛 - 修复 bug
-  ✨ - 引入新功能
-  🍎 - 修复 MacOS 下的问题
-  📝 - 写文档
-  🚀 - 部署新功能
 
-  ✅ - 添加测试用例
-  🔖 - 发版/版本标签
-  🔒 - 修复安全问题
-  🐧 - 修复 Linux 下的问题
-  🚨 - 移除 linter 的警告
-  🚧 - 工作在进行中
-  💚 - 修复 CI 构建问题
-  ⬇️ - 降级依赖库

-  🏁 - 修复 Windows 下的问题
-  ⬆️ - 升级依赖库
-  👷 - 添加 CI 构建系统
-  🔧 - 改变配置文件
-  🔨 - 大重构
-  🎉 - 初次提交
-  💄 - 升级 UI 和样式文件

其他参考：
http://www.blskye.com/Home/Blog/index.shtml?catword=git
https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
