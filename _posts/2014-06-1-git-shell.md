---
title:  "Git 命令"
author: luna
layout: post
categories: tools
tags: git

---


###Git 前的配置git config
	
	
	$ git config --global user.name "huina.gu"
	$ git config --global user.email huina.gu@qunar.com
	￼$ git config --global core.editor vim
	$ git config --global merge.tool vimdiff //差异分析工具
	$ git config --list //查看配置信息
	
###获取帮助	
	$ git help <verb>
	$ git <verb> --help 
	$ man git-<verb>
	
###Git 基础
	$ git clone git://github.com/schacon/grit.git //克隆仓库
	$ git status //检查当前文件状态
	$ git add README //跟踪新文件
		
	//查看已暂存和未暂存的更新
	$ git diff
	$ git diff --cached   
	$ git diff --staged 
	￼$ git commit //提交更新
	$ git commit -a -m 'added new benchmarks' //跳过使用暂存区域
	$ rm grit.gemspec 
	$ git rm grit.gemspec //移除文件
	$ ￼git mv file_from file_to//移动文件
	
	//查看提交历史
	$ git log		
	$ git log –p -2 //-p 选项展开显示每次提交的内容差异,用 -2 则仅显示最近的两次更新
	$ git log --stat //--stat,仅显示简要的增改行数统计
	$ git log --pretty=oneline //可以指定使用完全不同于默认格式的方式展示提交历史 oneline,short,full,fuller 
	$ git log --pretty=format:"%h - %an, %ar : %s"
	$ git log --since=2.weeks //限制输出长度
	
	//撤消操作
	$ git commit --amend //修改最后一次提交
	$ git reset HEAD benchmarks.rb //取消已经暂存的文件
	$ git checkout -- benchmarks.rb	 //取消对文件的修改
	
	//远程仓库的使用
	$ git remote -v //查看当前的远程库
	$ git remote add pb git://github.com/paulboone/ticgit.git  //添加远程仓库	$ git fetch [remote-name]  //从远程仓库抓取数据
	$ git push origin master //推送数据到远程仓库
	$ git remote show origin //查看远程仓库信息
	$ git remote rename pb paul //远程仓库重命名
	$ git remote rm paul //远程仓库的删除
	
	//打标签
###Git 分支	
	$ git branch testing  //创建一个新的分支