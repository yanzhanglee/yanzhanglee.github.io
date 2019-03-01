---
title: "Website Design - Patent Novelty"
image: 
  path: ./images/patent-novelty-screenshot.png
  thumbnail: ./images/patent-novelty-screenshot-small.png
  caption: "Website Screenshot"
---
- The website is now available. [View website](http://www.innogps.com/innovelty/index.html) <br>
- <i class="fab fa-github"></i> [Code Resource](https://github.com/yanzhanglee/Patent-Novelty-Website)

> I did this design project during my outbound exchange period in Singapore University of Technology and Design (SUTD), with the guide of Prof.Luo Jianxi. Generally speaking, I redesigned **the structure of the website** as well as **the visual part**, and put the design into practice by **building the website** based on my design. Please forgive me for the low quality of some parts of the website, because of my naive design experience and poor deleloping skill. <br>
> 这是我在新加坡科技设计大学（SUTD）交换时的科研项目，指导教授为Luo Jianxi教授。总体上看，我基于用户体验重新设计了网站的结构与视觉，并使用自己的前端开发技能付诸实践。该网站现已上线，可以在下方的链接中尝试使用或者是获得源码。必须承认，囿于开发水平和设计经验，网站中有太多不成熟和不够细致的地方，请见谅。

# Schema 大纲
**[Understand the theory 理解原理](#understand-the-theory-理解原理)**
**[Design 设计](#design-设计)**
**[Develop 开发](#develop-开发)**
**[Improvement 用户调研、反馈与迭代](#improvement-用户调研反馈与迭代)**
**[Shortcoming & Take Away 缺点与学习](#shortcoming&take-away-缺点与学习)**


# Understand the theory 理解原理
这个网站旨在使用一种新型独特的测量方式来测量一个专利的潜在价值。这个测量方式是由SUTD-MIT国际设计中心（[IDC](https://idc.sutd.edu.sg/)）的Luo Jianxi教授与He Yuejun博士研究发现的，相关论文如下：
<br>
- [Yuejun He, Jianxi Luo (2017) The Novelty “Sweet Spot” of Invention. Design Science, 3, e21.](https://www.cambridge.org/core/journals/design-science/article/novelty-sweet-spot-of-invention/48206051FC302693D375AB151B3BA9C7)
- [Yuejun He, Jianxi Luo (2018) Assess Novelty of An Invention Using the Central-Extreme Novelty Matrix: A Case Study of Juvo Lab’s Fibre-Optic Sensor Mat. ICDC, 2018, Bath, UK.](https://www.designsociety.org/publication/40709/ASSESS+NOVELTY+OF+AN+INVENTION+USING+THE+CENTRAL-EXTREME+NOVELTY+MATRIX%3A+A+CASE+STUDY+OF+JUVO+LAB%27S+FIBRE-OPTIC+SENSOR+MAT)

专利刚被申请时，很难在短期内判断其商业价值，一般来说都需要10年以上的时间才能得到确认。研究发现的这种新型方法指出，使用文中所述的两个变量——专利新颖程度的“极值”与“中心值”——进行专利“坐标”的标定，专利价值的分布有规律可循，其中有价值专利密度最高的区域被称之为“Sweet Spot”。
<br>
原始的网站如下图所示，图中的矩阵使用蓝色边框将“Sweet Spot”区域框出。用户输入专利的ID或者是关键词，再对对应的专利进行查询，它在矩阵中的位置会对应高亮。如果它位于蓝色区域中，那么它的潜在价值可能是较大的。
![原始网站 Original Website](http://img.oh-eureka.com/pics/2019-02-27-original-website.jpg)

在阅读文献的过程中，我发现实际上论文中已经给出了一张完整的专利潜在价值分布图。所谓的“Sweet Spot”只是其中最集中的一块区域，但其周边的深色区域较浅色区域，专利的潜在价值依然较大。那么为什么不直接将专利的对应分布直接地告诉用户呢？否则，对用户来说，专利便只有“在区域内”和“在区域外”两种情况。经过和教授讨论，这样的方式是可行的。于是接着进入了设计阶段。
![专利分布 Patent Distribution](http://img.oh-eureka.com/pics/2019-02-27-patent-distribution.png)

# Design 设计

建立在对论文和评估方法有一定了解的基础上，我的设计步骤如下：
- 分析原网站用户交互流程
- 设计用户交互流程
- 设计网站框架
- 制作视觉稿

## Analyze Original Website 分析原网站用户交互流程
![原网站 Original Website](http://img.oh-eureka.com/pics/2019-02-27-original-website-view.png)
根据对原网站的体验，我将用户交互流程制作如下图：
![用户交互流程 User Interaction Journey](http://img.oh-eureka.com/pics/2019-02-27-original-user-journey.png)
可以发现，用户在使用的过程中会产生诸如：什么是专利的新颖性？网站是怎么衡量它的？专利的ID是什么？专利的关键词是什么？等问题。<br>

## Design User Interaction 设计用户交互流程
该网站的本质是一个工具，其核心在于提供专利价值的衡量。对于一个工具，可以暂时简单地把用户分为小白用户(Naive User)与熟练用户(Skillful User)两类。针对熟练用户，网站需要做到快速响应，让用户的操作流畅而完整；针对小白用户，则需要首先解答“网站是做什么的？”这个问题，同时教育用户并建立信任感。对此，我计划使用一个**Demo**进行案例教学，并提供**How it works**这个部分进行评估原理的简单讲解。<br>
新的用户交互流程如下：
![用户交互流程设计 User Interaction Journey](http://img.oh-eureka.com/pics/2019-02-27-new-user-journey-1.png)

## Design Web Structure 设计网站框架
结合用户交互流程，网站框架如下：
- Home 主页
  - Search Patent ID 搜索专利ID
  - Search Keywords 搜索关键词
- Demo 案例
  - Select a Patent 选择专利
  - View Result 查看结果
- How it works 原理
- About 关于

## Visual Design 制作视觉稿
随后，我使用Ai制作了网页的视觉稿，并结合教授的意见进行了反复修改。在制作视觉稿的过程中，我结合自学的前端知识，尽量避免了“做不出来的设计”。（当然，更多是由于我自身技术能力的不足）

# Develop 开发
除去导航栏等小部件，我将需求分为了以下几个主要部分，并按顺序进行开发：
## Demo
![Demo 页面1](http://img.oh-eureka.com/pics/2019-02-27-DEMO1.jpg)
当用户的Cookie判断为第一次浏览该页面时，进入Demo页面。Demo页面希望呈现出三个专利供用户选择。这三个专利需要满足一些条件，比如专利本身或者专利对应的产品要有足够的知名度，同时专利自身在测量矩阵上的分布要在高价值区域。希望通过这样的方式，让用户测试一个专利，并获取相应的信息，在教学的同时建立测量机制的可信度。<br>
在花费了大量的时间之后，我选择了比较合适的三个专利。对专利视觉信息的呈现也做了一定的组织安排。在实现方面，基本是通过css来实现的。为了让网页显得更加具有焦点和富有科技感，我引用了particle.js，在网页的背景制作了可与鼠标交互的粒子动效。<br>
![Demo 页面2](http://img.oh-eureka.com/pics/2019-02-28-DEMO2.jpg)
选择其中一个专利进行测量之后，详情页面会介绍测量的结果。除去专利本身的信息外，也会呈现该专利与现实世界中具体产品应用的关系。通过这个页面，希望让用户明白网站中矩阵坐标、对应颜色与产品潜在价值的映射关系，同时建立对这样的评价体系的信任。

## Home
主页提供输入专利ID或者关键词进行搜索的功能，显示界面应该包括左侧的矩阵位置和右侧的专利信息。在原版的基础上，我做了如下的优化：
- 将Keywords和ID的输入框进行微调
- 将原本不具有强度的矩阵转换为现在具有强度的矩阵，通过颜色表示价值高低
- 将专利信息的呈现进行调整

![Search Patent ID](http://img.oh-eureka.com/pics/2019-03-01-ID.jpg)
![Search Keywords](http://img.oh-eureka.com/pics/2019-03-01-KEYWORD.png)

## How it works
How it works页面的本意是通过一个页面介绍论文中用于衡量专利价值的方法。由于对信息的理解和表达能力的限制，这个页面的完成度并不高，故在此处就不展示了，有兴趣可以前往http://www.innogps.com/innovelty/how_it_works.html 查看。

# Improvement 用户调研、反馈与迭代
第一版的网站并非是如前文图示那样的。在信息呈现方式上与现在的版本有着较大的差距，遗憾的是我没有保存网页的前一版本。具体来说，做了如下的改变：
- 将原版本中的Demo中三个专利的布局和呈现方式做了改变
- 将Demo中专利详情页的布局和呈现做了改变
- 调整了Home中Keywords搜索的呈现方式

这些改变是建立在我将网页发给2位设计专业的同学和2位外专业的朋友的反馈的基础上的，根据他们对网站意图和视觉呈现的评价，我做出了相应的改变。

# Shortcoming & Take Away 缺点与学习
最大的不足之一是由于自学前端经验不足，所有页面没有使用开发框架，所以没有做移动端适配，在小尺寸的屏幕上会出现形变。此外，由于前端实践的时间与精力需求对于我来说远高于设计的，在设计方面有很多细节没有做到位。<br>
相对的，第一次独立完成了网页的设计与开发，在很多细节上有了自己的认知与把控，并确立了继续学习React等开发框架的计划。

