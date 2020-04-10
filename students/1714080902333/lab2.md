# 实验二：用例建模

## 一、实验目的
1. 继续学习使用markdown编辑实验报告
2. 明确选题
3. 学习StarUML完成用例建模

## 二、实验内容
1. 创建用例图
2. 完成实验报告文档
3. 完成用例规约

## 三、实验步骤
1. 选题为HTTP Server
2. 根据选题创建用例图（Use Case Diagram）
3. 确定参与者（Actor）
    - 浏览器
4. 确定用例（Use Case）
    - 获取页面
    - 重写URL
5. 建立Actor与Use Case的关联
6. 完成用例规约（Use Case Specification）

## 四、实验结果

### 1. Use Case Diagram
![lab2-HTTP_UseCaseDiagram](./lab2_UseCaseDiagram.jpg)

### 2. Use Case Specification

**Specification 1**: 获取页面

| 用例编号 | UC01 | 备注 |
| ------- | ---- | --- |
| 用例名称 | 获取页面 |  |
| 前置条件 | 浏览器与服务器成功建立TCP连接 | 必须 |
| 后置条件 |  |  |
| 基本流程 | 1. 浏览器向服务器发送请求报文 | 用例正常处理流程 |
| ~ | 2. 服务器获取浏览器请求报文 | |
| ~ | 3. 服务器解析请求报文成功，查找页面文件 | |
| ~ | 4. 服务器查找页面文件成功，准备响应报文 | |
| ~ | 5. 服务器向客户端发送响应报文 | |
| ~ | 6. 浏览器获取响应报文，显示页面 | |
| 拓展流程 | 3.1 服务器解析请求报文失败，发送状态码400响应报文 | 用例执行异常 |
| ~ | 4.1 服务器查找页面文件失败，发送状态码404响应报文 | |

**Specification 2**: 重写URL

| 用例编号 | UC02 | 备注 |
| ------- | ---- | --- |
| 用例名称 | 重写URL |  |
| 前置条件 | 浏览器与服务器成功建立TCP连接 | 必须 |
| 后置条件 |  |  |
| 基本流程 | 1. 浏览器向服务器发送URL | 用例正常处理流程 |
| ~ | 2. 服务器获取URL | |
| ~ | 3. 服务器匹配URL成功，重写URL | |
| ~ | 4. 服务器向客户端发送重写后的URL | |
| ~ | 5. 浏览器获取URL | |
| 拓展流程 | 3.1 服务器匹配URL失败，向客户端发送原URL | 用例执行异常 |