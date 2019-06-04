## Git 安装
- 官网下载安装包进行安装

## 初始化Git仓库
 - 这个仓库会存放,git对我们项目代码备份的文件
 - 在项目目录右键打开 git bash here
 - 命令 : `git init`


 ## 自报家门
 - 就是在git中设置当前使用的用户是谁
 - 每一次备份都会把当前备份者的信息存储起来 
 - 命令:
   + 配置用户名: `git config --global user.name "xiaoming"`
   + 配置邮箱: `git config --global user.email "xm@qq.com"`


## 把代码存储到.git仓库中
- 1. 把代码放到仓库的门口(暂存区)
  + `git add ./readme.md` 把指定的文件放到暂存区
  + `git add ./` 把所有修改的文件添加到暂存区
- 2. 把仓库门口的代码放到里面的房间(版本库)里去
  + `git commit -m "这是对这次添加的东西的说明"`
## 可以一次性把我们修改的代码放到房间里(版本库)
  - `git commit --all -m "一些说明"`
    + --all 表示把所有修改的文件提交到版本库(不用add)  
## 查看当前的状态
- 可以用来查看当前代码有没有被添加放到仓库中去
- 命令: `git status`

## git 中忽略文件
- .gitignore, 在这个文件中可以设置要被忽略的文件或者目录
- 被忽略的文件不会被提交到仓库里去
- 在.gitignore中可以书写要被忽略的文件的路径,以/开头,一行写一个路径,,这些路径所对应的文件都会被忽略,不会被提交到仓库中
+ 写法:
     * `/.idea` 会忽略.idea文件
     * `/js` 会忽略js目录里的所有文件
     * `/js/*.js` 会忽略js目录下的所有js文件

 ## 查看日志
  - `git log ` 查看历史提交的日志
  - `git log --oneline` 可以看到简洁版的日志

## 回退到指定的版本
- `git rest --hard Head~0`
   + 表示回退到上一次代码提交时的状态
- `git rest --hard Head~1`
   + 表示回退到上上次代码提交时的状态

- `git reset --hard [唯一标识(版本号)]`
	+ 可以通过版本号精确的回退到某一次提交时的状态

- `git reflog`
	+ 可以看到每一次切换版本的记录: 可以看到所有提交的版本号


	### Github
	- https://github.com
	- 不是git,只是一个网站
	- 只不过这个网站提供了允许别人通过git上传代码的功能


### 提交代码到github(当作git服务器来用)
 - `git push [地址] master`
    + 示例 : `git push https://github.com/shiweiquan/test1.git master`;
    + 会把当前分支的内容上传到远程的master分支上

- `git pull [地址] master`
	+ 示例:	 `git pull https://github.com/shiweiquan/test1.git master`
	+ 会把远程分支的内容获取到本地(*注意本地要先初始化一个仓储*)