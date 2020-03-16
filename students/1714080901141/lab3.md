# 实验名称：过程建模
## 一、实验目标
#### 1. 掌握过程建模的方法；
#### 2. 掌握活动图的画法。
## 二、实验内容
#### 1. 记过程建模学习笔记；
#### 2. 回顾用例建模的过程；
#### 3. 联系过程建模和用例建模；
#### 4. 画活动图。
## 三、实验步骤
#### 1. 观看录制视频、琢磨课堂文档：

（1）学习来源：  
- [bilibili实验3的录播课程集](https://b23.tv/av96420419/p1)  
- [实验3内容及讲义](https://github.com/hzuapps/uml-modeling-2020/issues/3)

（2）学习笔记：  
- 初始结点：是虚拟的，用实心圆表示，表示活动的开始  
- 结束结点：是虚拟的，用实心加圆圈表示，表示活动的结束  
- 流程线：用带箭头的实线表示，表示顺序执行活动  
- 决策：用菱形表示，表示分不同情况执行，并且从决策出去的带箭头的实线要标注活动执行的条件；推荐成对使用菱形表示决策  
- 活动：用圆角的矩形表示，表示操作步骤  

#### 2. 回顾lab2.md：

- lab2.md中有两个用例归约，名称分别是“添加航班”和“取消航班”  
- 每个用例规约都有“基本流程”和“拓展流程”两部分  
- 用例规约中的每一个步骤必须是操作，不能是状态（如：管理员等待状态）  

#### 3. 思考用例建模和过程建模的关系：

- 用例规约的步骤顺序，表明了实线箭头方向  
- “拓展流程”和“基本流程”用菱形（决策）表示，并且条件要注明  

#### 4. 活动图制作步骤如下：

（1）创建Activity Diagram：打开staruml -> model右键 -> Add Diagram -> Activity Diagram  
（2）添加初始结点：Toolbox -> Activities(Basic) -> Initial  
（3）添加结束结点：Toolbox -> Activities(Basic) -> Final  
（4）添加活动：Toolbox -> Activities(Basic) -> Action  
（5）分支处添加决策：Toolbox -> Activities(Basic) -> Decision  
（6）添加流程线：Toolbox -> Activities(Basic) -> Control Flow（在决策分支处注明条件）  
（7）调整整体：调整流程线的样式，活动的位置  

## 四、实验结果

#### 1. 活动图1：添加航班
![Activity Diagram1](./lab3_ActivityDiagram1.jpg)  
#### 2. 活动图2：取消航班
![Activity Diagram2](./lab3_ActivityDiagram2.jpg)  

## 五、实验总结

#### 1. 过程建模的方法如下：
- 依据用例规约的基本流程和拓展流程，实现过程建模
#### 2. 活动图画法如下（画法顺序不唯一）：
- 创建Activity Diagra -> 添加初始结点、添加结束结点 -> 添加活动、分支处添加决策 -> 添加流程线、调整整体
#### 3. 决策前应有类似检查的动作
## 六、实验调试
#### Q1:
what:  
决策错误地使用粗直线而非菱形表示  
why:  
粗直线表示的是可并发，多线程的；菱形表示的是多种情况的决策  
how:  
用成对的菱形替换掉粗直线  
#### Q2:
what:  
删除本地库的model1.jpg和model2.jpg之后，push操作不能实现github个人帐号下的修改  
why:
git本读磁盘分为暂存区和工作区，push是将暂存区推到个人帐号的；而平常操作的是工作区，这就需要类似于add或者rm操作，将工作区指定文件保存起来了  
how：  
``` bash
git rm -f model1.jpg model2.jpg #remove from stage
git commit -m "delete model1.jpg and model2.jpg"
git push
```
#### Q3:  
what：
为方便老师查看有可能需要反复修改的图片，需要学会在pull request的commit中显示图片，但是不知道如何读取图片的路径  
why：  
事实上，当用户pull request后，文档路径会在https://raw.githubusercontent.com/用户帐号名/主库名/blob/master 下  
how： 
```
![ActivityDiagram1](https://raw.githubusercontent.com/cyh1069247088/uml-modeling-2020/master/students/1714080901141/lab3_ActivityDiagram1.jpg)
![ActivityDiagram2](https://raw.githubusercontent.com/cyh1069247088/uml-modeling-2020/master/students/1714080901141/lab3_ActivityDiagram2.jpg)
```
