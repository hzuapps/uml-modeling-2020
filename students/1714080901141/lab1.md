# 实验一
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
4. 在Ubuntu的Terminal
```bash
#install git
sudo apt-get install git
#connect the name and user
git config --global user.name "cyh10692470888"
git config --global user.email "10692470888@qq.com"
#clone
git clone https://github.com/cyh1069247088/uml-modeling-2020
#create lab1
cd uml-modeling-2020/students
mkdir 1714080901141
touch lab1.md
```
5. 在[StarUML官网](http://staruml.io/)下载[系统对应版本](http://staruml.io/download/releases/StarUML-3.2.2.AppImage)
```bash
#Download for Linux(64 bit)
wget http://staruml.io/download/releases/StarUML-3.2.2.AppImage
#Run StarUML
./StarUML-3.2.2.AppImage
```
6. 在StarUML下
- Model -> Add Diagram -> Class Diagram
- Add Class Three Times
- File -> Export Diagram As -> APEG...
- Choose uml-modeling-2020/students/1714080901141
- Rename "model1.jpg"
7. 在lab1.md中使用图片
- Adding
```
![第一个UML图](./model1.jpg)
```
## 四、实验结果

![第一个UML图](./model1.jpg)

## 五、实验收获
1. 养成良好的写实验的习惯，即明确的实验目的，全面的实验内容，细致的实验步骤，明了的实验结果，简洁的实验总结。
2. git pull用来刷新本地库，使本地库与个人库同步。
3. git push用来刷新个人库，使个人库与本地库同步。
