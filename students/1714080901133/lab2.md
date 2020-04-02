# 实验二

## 实验目标
- 细化选题
- 使用Markdown撰编写报告
- 使用StarUML用例建模

## 实验内容
  1.新增器材信息创建用例图

  2.新增器材信息编写实验报告文档

  3.新增器材信息编写用例规约

## 实验步骤
  1.新增器材信息在StarUML绘制图。
  2.新增器材信息确定参与者
      - 管理员   
  3.新增器材信息确定用例（UserCase）:   
      - 新增教学器材
      - 分配教学器材
      - 查询教学器材
      
  4.导出图片为jpg格式

  5.在Sublime Text编写文档和表格

  6.git push到GitHub

  7.pull request，请求合并到主仓库

## 实验结果
![第二个UML图](./model2.jpg)


## 表1：新增教学器材用例规约  

用例编号  | UC01 | 备注  
-|:-|-  
用例名称  | 新增器材  |   
前置条件  |     | *可选*   
后置条件  |      | *可选*   
基本流程  | 1.管理员点击新增器材按钮；  |*用例执行成功的步骤*    
~| 2.系统显示新增器材页面；  |   
~| 3.管理员输入器材名的信息，点击确认按钮；  |   
~| 4.系统查询器材信息，检查器材名不存在，保存新增器材信息；  |   
~| 5.系统向管理员提示“添加成功”。  |  
扩展流程  | 4.1系统发现器材名已存在，提示管理员“器材已存在”。 |*用例执行失败* 



## 表2：分配教学器材用例规约  

用例编号  | UC02 | 备注  
-|:-|-  
用例名称  | 分配器材  |   
前置条件  |      | *可选*   
后置条件  |      | *可选*   
基本流程  | 1.管理员点击分配教学器材按钮；  |*用例执行成功的步骤*    
~| 2.系统显示分配器材页面；  | 
~| 3.系统查询到可分配的器材；   |  
~| 4.系统查询到可分配的课室；   | 
~| 5.管理员点击所要分配的器材和课室；  |    
~| 6.系统向管理员提示“分配成功”。  |  
扩展流程  | 3.1系统查询不到可用于分配的器材，提示“没有器材可以分配”；  |*用例执行失败* 
~| 4.1系统查询不到可用于分配的课室，提示“没有课室可以分配”。   | 

## 表3：查询教学器材用例规约  

用例编号  | UC03 | 备注  
-|:-|-  
用例名称  | 查询器材  |   
前置条件  |      | *可选*   
后置条件  |      | *可选*   
基本流程  | 1. 管理员点击更查询教学器材按钮；  |*用例执行成功的步骤*    
~| 2.系统显示查询器材页面；  | 
~| 3. 管理员输入所要查询的教学器材；  |  
~| 4. 系统检查该教学器材存在，系统显示该器材的使用信息。   |    
扩展流程  | 4.1 系统检查该教学器材不存在，提示管理员“此教学器材不存在”。 |*用例执行失败* 


