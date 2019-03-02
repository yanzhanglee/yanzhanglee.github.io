---
title: "Android App - Class Attendance Assistant"
image: 
  path: http://img.oh-eureka.com/pics/2019-03-02-poster.jpg
  thumbnail: http://img.oh-eureka.com/pics/2019-03-02-poster-little.png
  caption: "Android App"
---
**An Android App sulution to class attendance and more.**<br>
**一个旨在解决课堂签到问题的安卓App**

<i class="fab fa-github"></i> Code Resource
- [Face Detection Attendance Website 签到系统网页](https://liyanzhang.cn/Smart-Class-Attendance-Web-end/)
- [Website Code](https://github.com/yanzhanglee/Smart-Class-Attendance-Web-end/tree/master)
- [Android App Code](https://github.com/yanzhanglee/Smart-Class-Android-App)

> This is a course project in the course *Introduction to Information System and Programming* in ISTD major, SUTD. The course is about Java Programming, Android Develop and Object Oriented Programming. The final project of the course is designing and building an Android App related to IoT and AI. We, a group of 3, developed an App aiming at solving the class attendance problem with face detection, as well as the class participation problem. Generally speaking, I designed the major functions and interaction of the App, the visual interface, the poster and was fully in charge of the front-end developing and 2 of 4 app functions developing. The projects has been selected to the ISTD major show next year as an excellent work.<br>
> 这是新加坡科技设计大学信息计算机专业的专业课——信息系统编程介绍的课程项目。这门课介绍了Java编程，安卓开发以及面向对象编程的基本原理。课程的最终项目要求产出一个安卓App，并需要与IoT（物联网）以及AI（人工智能）有关。我们小组（3位主要成员）开发了一款旨在解决课堂签到和课堂参与问题的App。总体上看，我负责了**主要功能的定义、交互设计，所有界面的视觉设计，海报设计，并负责了网页前端（用于面部识别）的开发和2个App功能的开发**。我们的项目被选中作为ISTD下一年课程展览的优秀作品。

# Schema 大纲
**[Brief Introduction 概览](#brief-introduction-概览)**
<br>
**[Design and Logic 设计与实现思路](#design-and-logic-设计与实现思路)**
<br>
**[Showcase 演示](#showcase-演示)**

# Brief Introduction 概览
首先请通过浏览课程海报来对项目内容进行基本的了解。<br>
Please refer to the poster to have a glance on the project.
![Poster](http://img.oh-eureka.com/pics/2019-03-02-poster.jpg)

# Design and Logic 设计与实现思路
## Face Detection Attendance 人脸检测签到端
计划采用前端作为签到端，使用getUserMedia()调用摄像头定时拍照，将照片使用POST方法向Face++ Web API请求，返回照片中人脸的Token和置信度，进行判断后显示签到成功或失败。对应地，更新前端界面显示，并向队友搭建的SQLite Post相关同学签到成功的结果。

## Android App 安卓App
安卓App从主要有四个功能，其一为显示最近的课程的倒计时，并实时从服务器获取同学的签到状态，将签到的同学用RecyclerView显示在界面上；其二为过去所有课程的CardView，从本地Json文件获取课程信息，进行处理后显示。数据结构如下：
```json
{ "name": "50.001 Introduction to Information System and Programming",
    "session": "CI01",
    "date": "11/12/2018",
    "timing": "09:00",
    "venue": "2.502, SUTD",
    "studentNumber":"50",
    "studentStatus":{"LiYanzhang":"True","WangTianduo":"False","TangXiaoyue":"False","visitor":"True","visitor":"True","visitor":"True","visitor":"True","visitor":"True","visitor":"True","student1":"False","student2":"False","student3":"False","student4":"False","student5":"False","student6":"False"}},
```
其三为日历，同样是将本地Json文件中的课程数据提取并显示在对应的日历上；其四是为了现场Demo效果的功能，可以现场向Face++和SQL database添加人脸与Id，并且现场演示签到成功。

# Showcase 演示
![Showcase](http://img.oh-eureka.com/pics/2019-03-02-%E5%B1%95%E7%A4%BA-1.png)
在展示中，我们想老师完整地呈现了精心安排的流程：<br>
同学刷脸 - 扫描端显示成功 - App端显示成功 - 老师刷脸 - 刷脸失败 - App添加老师人脸信息 - 老师刷脸 - 扫描端显示成功 - App端显示成功 <br>
此外，还展示了对应的日程界面，课程信息界面等等。


