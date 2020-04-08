# GitHub实验操作步骤

## 1. 注册GitHub帐号

- 打开 https://github.com，注册（Signup）新帐号；
- 在设定的邮箱接收激活邮件，点击激活链接，激活新帐号。

## 2. Fork 实验库

- 打开 https://github.com/hzuapps/uml-modeling-2020  
- 点击右上角的 Fork 按钮，将项目复制到个人帐号下：

```  
https://github.com/你的帐号名/uml-modeling-2020  
```  

## 3. 安装 Git 工具

- 打开 https://git-scm.org ，下载适合本机版本（32位或64位）；
- 双击 exe 文件将工具安装到本机上；
- 从开始菜单打开 Git-Shell。

## 4. 克隆代码到本地磁盘

- 用 cd 命令切换到保存代码的路径上，如切换到D盘：   
```   
$ cd d: 
```   
- 用 clone 命令将个人库的代码克隆到本地磁盘：  
```   
$ git clone https://github.com/你的帐号名/uml-modeling-2020
```   
- 进入本地项目源代码目录：  
```   
$ cd uml-modeling-2020
```   

## 5. 编写代码

- 选择下载并安装一个网页编辑工具，如：Sublime-text
- 打开资源浏览器，在项目中创建个人学号目录，如：uml-modeling-2020/students/123456/
- 或者直接在命令行里，使用 mkdir 命令创建目录：  
```   
$ mkdir students/123456 
```   
- 创建一个Markdown文件，如： students/123456/lab1.md    

## 6. 提交代码

```  
$ git add students/123456/*
$ git commit -m "创建第一个建模文档"
$ git push
```  

注意：第一次操作时，如果遇到错误提示，则按照提示配置全局邮箱地址及用户名：

```  
$ git config --global user.email "你的邮箱"   
$ git config --global user.name "你的帐号名"   
```  
然后再继续执行之前出错的命令   
```   
$ git commit -m "创建第一个建模文档"
$ git push
``` 

注意：提交代码可以用通配符 * 和 ? 

```  
$ git add students/123456/**
```  

注意：删除多余文件或文件夹的命令；即使硬盘里面已经删掉也要执行命令（想想为什么？）。

```  
$ git rm -rf students/学号目录/你不要的文件
$ git rm -rf 你传错或不要的文件夹/**
$ git commit -m "删除不必要的文件"
$ git push
```  

## 7. 发送合并请求

- 打开个人项目库：https://github.com/你的帐号名/uml-modeling-2020 ；
- 点击 New pull request 按钮；
- 检查自己所修改的文件是否正确。如果不正确，则按照之前的步骤重新修改；如果正确，则点击『Create pull request』绿色按钮。
- 在发帖子表单中填写以下信息：
```  
Title：#1 提交实验一代码
Leave a comment：选填
```  

## 8. 最后一步

Pull request发送之后，一定要自己查看自己修改过的文件，看看有没有改错文件（Files changed）。

![image](https://user-images.githubusercontent.com/627946/54257709-37355400-459b-11e9-8547-f03935f07a61.png)

