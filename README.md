# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10986ssm旅游网站

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=83)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

旅游网站系统工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。旅游网站系统的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、用户信息：用户名、密码、姓名、性别、头像、手机、邮箱、身份证，实体图如图4-3所示：

![](/md/blog.014.png)

图4-3用户信息实体图

2、景点信息：景点名称、分类、景点图片、景点星级、景点地址、门票价格、营业时间、注意事项、景点介绍，实体图如图4-4所示：

![](/md/blog.015.png)

`   `图4-4 景点信息实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 allusers表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|username|varchar|50|` `default NULL|
|pwd|varchar|50|` `default NULL|
|cx|varchar|50|` `default NULL|


表4-2 jingdianpingjia表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|jingdianmingcheng|varchar|50|default NULL|
|fenlei|varchar|50|default NULL|
|jingdiantupian|varchar|50|default NULL|
|menpiaojiage|varchar|50|default NULL|
|zongjiage|varchar|50|default NULL|
|jingdianpingfen|varchar|50|default NULL|
|jingdianpingjia|varchar|50|default NULL|
|yonghuming|varchar|50|default NULL|
|shouji|varchar|50|default NULL|

表4-3：jingdianxinxi表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|jingdianmingcheng|varchar|50|default NULL|
|fenlei|varchar|50|default NULL|
|jingdiantupian|varchar|50|default NULL|
|jingdianxingji|varchar|50|default NULL|
|jingdiandizhi|varchar|50|default NULL|
|menpiaojiage|varchar|50|default NULL|
|yingyeshijian|varchar|50|default NULL|
|zhuyishixiang|varchar|50|default NULL|
|jingdianjieshao|varchar|50|default NULL|


表4-4：lvyouzhoubian表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|jiudianmingcheng|varchar|50|default NULL|
|leibie|varchar|50|default NULL|
|xingji|varchar|50|default NULL|
|jiudiantupian|varchar|50|default NULL|
|jiudiandizhi|varchar|50|default NULL|
|lianxidianhua|varchar|50|default NULL|
|jiudianjieshao|varchar|50|default NULL|

表4-5：yonghu表

|列名|数据类型|长度|约束|
| :-: | :-: | :-: | :-: |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|yonghuming|varchar|50|default NULL|
|mima|varchar|50|default NULL|
|xingming|varchar|50|default NULL|
|xingbie|varchar|50|default NULL|
|touxiang|varchar|50|default NULL|
|shouji|varchar|50|default NULL|
|youxiang|varchar|50|default NULL|
|shenfenzheng|varchar|50|default NULL|

# 5统详细设计
## 5.1前台主页功能模块
旅游网站系统，在系统主页可以查看首页、景点信息、旅游周边、特色美食、新闻资讯、我的、跳转到后台、客服等内容，如图5-1所示。

![](/md/blog.016.png)

图5-1前台主页功能界面图



`    `用户注册，在用户注册页面可以填写用户名、密码、姓名、性别、手机、邮箱、身份证等信息进行注册，如图5-2所示。

![](/md/blog.017.png)

图5-2 用户注册界面图

登录，在登录页面通过填写账号、密码等信息完成登录，如图5-3所示。

![](/md/blog.018.png)

图5-3登录界面图

景点信息，用户在景点信息管理页面中可以查看景点名称、分类、景点图片、景点星级、景点地址、门票价格、营业时间、注意事项、景点介绍等信息，并可景点信息收藏、评论操作，如图5-4所示。


![](/md/blog.019.png)

图5-4景点信息界面图

特色美食，用户在特色美食页面中可以查看，并可特色美食收藏、评论操作，如图5-5所示。


![](/md/blog.020.png)

图5-5特色美食界面图


## 5.2管理员功能模块
管理员登录，通过填写注册时输入的用户名、密码进行登录，如图5-6所示。

![](/md/blog.021.png)

图5-6管理员登录界面图

管理员登录进入旅游网站系统可以查看主页、个人中心、景点分类管理、景点信息管理、旅游周边管理、特色美食管理、用户管理、门票预定管理、景点评价管理、管理员管理、系统管理等信息。如图5-7所示用户管理，

管理员对个人中心进行操作填写原密码、新密码、确认密码并进行添加、删除、修改以及查看，程序成效图如下图5-8所示:

![](/md/blog.022.png)

图5-7首页界面图

![](/md/blog.023.png)

图5-8修改密码界面图

景点信息管理，管理员在景点信息页面中可以查看景点名称、分类、景点图片、景点星级、景点地址、门票价格、营业时间、注意事项、景点介绍等信息，并可根据需要对已有景点信息管理进行修改或删除等操作，如图5-9所示。

![](/md/blog.024.png)

图5-9 景点信息管理界面图

旅游周边管理，管理员在旅游周边管理页面中可以查看添加、修改或删除等详细操作，如图5-10所示。

![](/md/blog.025.png)

图5-10旅游周边管理界面图

特色美食管理，管理员在特色美食管理页面中可以查看美食名称、美食类型、图片、打卡地点、人均消费、美食介绍等内容，并且根据需要对已有特色美食管理进行详情，修改或删除等详细操作，如图5-11所示。

![](/md/blog.026.png)

图5-11特色美食管理界面图

用户管理，管理员在用户管理页面中可以查看用户名、密码、姓名、性别、头像、手机、邮箱、身份证等内容，并且根据需要对已有用户信息进行详情，修改或删除等详细操作，如图5-12所示。

![](/md/blog.027.png)

图5-12用户管理界面图




系统管理:管理员通过系统管理页面查看客服中心、轮播图管理、旅游资讯等进行查看客服聊天、上传图片，资讯发行添加、删除、修改以及查看并对整个系统进行维护等操作，如图5-13所示。


![](/md/blog.028.png)

![](/md/blog.029.png)

图5-13用户管理界面图


## 5.3用户功能模块
用户登录进入旅游网站系统可以查看个人中心、门票预定管理、景点评价管理、我的收藏管理等内容。如图5-14所示。

![](/md/blog.030.png)

图5-14 首页界面图

用户信息，在用户信息页面中可以查看用户名、密码、姓名、性别、头像、手机、邮箱、身份证等信息，并且根据需要对已有用户信息进行查看删除等其他详细操作，如图5-15所示。

![](/md/blog.031.png)

图5-15用户信息界面图

门票预定管理，用户在门票预定管理页面中可以查看评价、支付操作，如图5-16所示。

![](/md/blog.032.png)

![](/md/blog.033.png)

图5-16门票预定管理界面图

我的收藏管理，在收藏管理页面可以查看用户ID、、收藏ID 表名 收藏名称、收藏图片等等内容，并进行查看、删除操作，如图5-17所示。

![](/md/blog.034.png)

图5-17我的收藏管理界面图















