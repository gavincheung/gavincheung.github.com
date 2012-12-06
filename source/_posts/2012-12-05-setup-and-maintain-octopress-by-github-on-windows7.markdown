---
layout: post
title: "在Windows7中用Github搭建和维护Octopress"
date: 2012-12-05 11:44
comments: true
categories: github octopress
---

## 搭建 Octopress

### 安装必要软件

1. git - 用于在 Github 上维护 Octopress
	* 最新版本的 git 安装程序可以在 [msysgit][git下载链接] 找到；
	* 本文发布时的最新版本为 Git-1.8.0-preview20121022，下载并安装之。

2. ruby - Octopress 的运行环境
	* ruby 安装程序可以在 [RailsInstaller][RailsInstaller链接] 找到；
	* Octopress 要求安装 [rubyinstaller-1.9.2-p290][ruby下载链接]，下载并安装之；
	* 确保`C:\Ruby192\bin`是否在Windows当前用户的`PATH`变量环境中。

3. 安装Devkit - 编译环境
	* 下载 [RubyInstaller DevKit][DevKit下载链接]，并按如下方法安装：
		+ 将 DevKit 自解压包释放到 C:\DevKit；
		+ 在 Windows CMD 窗口中 `cd` 到Devkit的解压目录并执行：`ruby dk.rb init`；
		+ 执行：`ruby dk.rb install`。

4. 安装 python - 代码加亮系统 pygments 需要 python 支持
	* 最新版本的 ActivePython 安装程序可以在 [ActivePython][ActivePython链接] 找到；
	* 本文发布时的最新版本为 ActivePython 2.7.2，下载并安装之;
	* 安装完毕后，在 Windows CMD 窗口中 `cd` 到 ActivePython 的 Script 目录并执行：`easy_install pygments`；

### 配置 Windows 运行环境

### 配置 ruby 运行环境

### 安装 Octopress

## 配置和使用 Octopress

### Octopress 的基本配置

### Octopress 的使用

* 创建新页面

* 编辑页面

* 首次提交

* 使用 rake 任务管理 Octopress

* 管理源码的仓库分支
	+ 提交 source 到 Github

			cd octopress
			git add .
			git commit -m "your message"
			git push origin source

	+ 注：如果用两台或以上的电脑进行 Octopress 的维护，则每一次都要先从 Github 上 pull 最新的内容，再进行编辑
	
			cd octopress
			cd _deploy
			git pull origin master
			cd ..
			git pull origin source

### 进一步配置 Octopress

## 参考资料

* [在 Windows7 下从头开始安装部署 Octopress][post_from_sinosmond]

[git下载链接]: http://code.google.com/p/msysgit/downloads/list
[RailsInstaller链接]: http://rubyforge.org/frs/?group_id=167
[ruby下载链接]: http://rubyforge.org/frs/download.php/75127/rubyinstaller-1.9.2-p290.exe
[DevKit下载链接]: https://github.com/downloads/oneclick/rubyinstaller/DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe
[ActivePython链接]: http://www.activestate.com/activepython
[post_from_sinosmond]: http://sinosmond.github.com/blog/2012/03/12/install-and-deploy-octopress-to-github-on-windows7-from-scratch/