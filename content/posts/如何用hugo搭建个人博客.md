---
title: "如何用hugo搭建个人博客"
date: 2019-11-22T17:01:52+08:00
draft: false
---

# 8. 【Git入门】个人博客搭建与域名购买
### 8.1 Hugo 搭建个人博客
- MAC 安装
	```bash
	brew install hugo
	hugo version
	```
- 看文档搞出网站
	*   进入[Hugo](https://gohugo.io/getting-started/quick-start/)官网, 跟着操作Step2到Step7
	1. 创建的文件名为 `xxx.github.io-generator`
	2. 中文配置为`zh-Hans` 
	* 得到一个public目录, 这就是我们博客站点
	* `hugo server -D` 可以预览草稿
	* `hugo server` 可以浏览非草稿
- 与`Github Pages`绑定
	* `xxx.github.io-generator`中创建`.gitignore`忽略`/public/`文件
	* 进入`public`后, `git`初始化
	* 创建`repo`名为`xxx.github.io-generator`
	* 连接`public`远程
	* 查看`git`中`setting`的`GitHub Pages`
- 换主题
	* 进入`hugo`[主题页面](https://themes.gohugo.io/)
	在 `xxx.github.io-generator`目录下`clone`
	* 下载好主题后,进行`hugo -D`
	* 然后进入`public`, 提交到`git`远程

### 8.2 购买域名
[namesilo(方便)](https://www.namesilo.com/)
- 取消自动续费
- 不保护隐私
- 除了邮箱信息真实外, 其他随意填.

### 8.3 域名配置
- 配置`DNS`
 * 把现有的无关配置删除
 * 配置四条`A`记录到`185.199.108.153`等`IP`
	`GitHub`上的[DSN](https://help.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site)
*	mac用户: `dig noall answer 域名 `
	出现刚配置的`DSN`

- 配置`GitHub Pages`
	* 添加域名
	* 不开启`HTTPS`
### 8.4 备份记录
将忽略了`public`的其他文件, 在GitHub上创建一个新的`repo`, 然后与之远程连接起来.