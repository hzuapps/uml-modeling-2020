# 实验一：UML建模工具 
## 一、实验目标
1. 熟悉github实验过程
2. 安装与使用StarUML
## 二、实验内容
1. 创建并提交lab1.md文档
2. 利用StarUML创建模型，并以图片格式导出模型
3. 在lab1.md中使用该图片
## 三、实验步骤
1. 登录[hzuapps/uml-modeling-2020](https://github.com/hzuapps/uml-modeling-2020)
2. 登录个人帐号
3. 在[hzuapps/uml-modeling-2020](https://github.com/hzuapps/uml-modeling-2020)下点击fork
4. 在Ubuntu的Terminal下:
```bash
#install git
sudo apt-get install git
#clone
git clone https://github.com/cyh1069247088/uml-modeling-2020
#create lab1
cd uml-modeling-2020/students
mkdir 1714080901141
touch lab1.md
```
5. 在[StarUML官网](http://staruml.io/)下载[系统对应版本](http://staruml.io/download/releases/StarUML-3.2.2.AppImage):
```bash
#Download for Linux(64 bit)
wget http://staruml.io/download/releases/StarUML-3.2.2.AppImage
#Run StarUML
./StarUML-3.2.2.AppImage
```
6. 在StarUML下:
- Model -> Add Diagram -> Class Diagram
- Add Class Three Times
- File -> Export Diagram As -> APEG...
- Choose uml-modeling-2020/students/1714080901141
- Rename "model1.jpg"
7. 在lab1.md中使用图片:
- Adding the following code in lab1.md.
```
![Diagram](./lab1_Diagram.jpg)
```
## 四、实验结果

![Diagram](./lab1_Diagram.jpg.jpg)

## 五、实验收获
1. 养成良好的写实验的习惯，即明确的实验目的，粗略但全面的内容的实验内容，细致的实验步骤，明了的实验结果，简洁的实验总结，深度的调试。
2. git pull用来刷新本地库，使本地库与个人库同步。
3. git push用来刷新个人库，使个人库与本地库同步。
## 六、实验调试
1. 
what:
git pull的时候，会报错如下：
```
Updating 1cc0009..db661fd
error: Your local changes to the following files would be overwritten by merge:
	students/1714080901141/lab1.md
Please, commit your changes or stash them before you can merge.
Aborting
```  
why:
如果系统中有一些配置文件在服务器上做了配置修改,然后后续开发又新添加一些配置项的时候,在发布这个配置文件的时候,会发生代码冲突  
how:
- Saving your local data
``` bash
git stash    #暂存当前正在进行的工作。
git pull origin master   #拉取服务器的代码
git stash pop   #合并暂存的代码
```
- Ovewriting your local data
```
reset --hard  #直接回退到上一个版本
git pull origin master   #拉取服务器的代码
```  
2. 
What: git clone operation is too slowly  
why: git clone特别慢是因为github.global.ssl.fastly.net域名被限制了。  
how:
- Indirectly
拜托你的朋友或老师帮忙
- Directly
码云、搭建服务器并配置代理
