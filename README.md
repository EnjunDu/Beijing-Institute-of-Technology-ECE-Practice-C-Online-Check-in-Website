# Beijing-Institute-of-Technology-ECE-Practice-C-Online-Check-in-Website
北京理工大学ECEB实践——制作二维码签到网站
# 二维码签到系统 #
#管理员入口的账号是sky，密码是sky666666#
#演示视频的url为：<https://www.bilibili.com/video/BV1vC4y1m72n/?buvid=XUCA727CB1A1FE79CA0F8C1D813712FE9A658&from_spmid=main.space-contribution.0.0&is_story_h5=false&mid=9I1LA3hoWIC72wb3O6CGWg%3D%3D&p=1&plat_id=114&share_from=ugc&share_medium=android&share_plat=android&share_session_id=9cdff248-b885-4563-b50c-6f27c275e028&share_source=WEIXIN&share_tag=s_i&spmid=united.player-video-detail.0.0&timestamp=1700223955&unique_k=wu3NDgF&up_id=435465864>


##可以看看
# 如果您运行了app.py， #
#第一个url是http://10.198.85.110:8848，如果您的校园网地址也是在北理良乡静园地区那么这个ip地址就可以跳转到登录页面，第二个二维码的url是http://localhost:8848，这个是根据您的ip来自动填充，不需要您手动输入ip，总之就是都可以吧#
# 概述 #
本项目基于Flask Web框架，实现了一个二维码签到系统。该系统具有以下功能：

* 根据url跳转二维码：点击url可以跳转到指定二维码
* 显示二维码：用户可以访问指定的URL以显示二维码。
* 扫描二维码：扫描二维码将用户重定向到登录页面。
* 用户认证：登录页面允许用户登录或注册账户。
* 签到功能：登录后，用户可以进行签到操作。
* 查询签到数据：系统提供了查询签到数据的功能。

## 文件结构 ##
项目包含以下文件：
1.app.py: 包含Flask应用程序的主要逻辑，定义了用户、签到记录等数据库模型，以及相关路由和视图。

2.templates 文件夹：包含所有HTML模板，用于渲染不同页面，包括用户登录、注册、签到等页面。

3.static 文件夹：包含静态文件，如样式表和背景图片。

4.在浏览器中访问 http://localhost:8848 查看项目。
## 
app.py 主要功能
 ##

* 导入模块和初始化应用程序：使用 Flask 创建 Web 应用程序、使用 SQLAlchemy 进行数据库交互。

* 定义两个数据库模型：User（用户信息）和 SignIn（签到记录）。

* 在每个请求之前创建数据库表格。

* 路由和视图函数：显示项目的主页、提供用户注册功能，用户可以填写用户名和密码进行注册、提供用户登录功能，用户可以输入用户名和密码登录系统、提供用户签到功能，用户登录后可以点击签到按钮完成签到、提供管理员登录入口，用于访问后台面板、显示管理员面板，包含签到记录的表格，用于查询签到数据、如果直接运行 app.py 文件，则启动 Flask 应用程序。


## html文件的主要功能 ## 
1. login.html

目的： 用户登录页面。

功能：

* 提供用户输入用户名和密码的表单。

* 包含登录按钮，用于提交登录请求。

* 包含注册链接和管理员入口。

2. register.html

目的： 用户注册页面。

功能：

* 允许用户创建新账号。

* 包含用户名和密码输入框。

* 包含注册按钮，用于提交注册请求。

3. signin.html

目的： 用户签到页面。

功能：

* 显示签到按钮，用户点击按钮完成签到。

4. admin_login.html

目的： 管理员登录页面。

功能：

* 提供管理员登录入口。

* 包含用户名和密码输入框。

* 包含登录按钮，用于提交管理员登录请求。

5. admin_dashboard.html

目的： 管理员面板页面。

功能：

* 显示签到记录的表格。

* 用于查询签到数据。


6. admin_dashboard.html

目的： 项目主页。

功能：

* 提供项目的主要入口。

* 可以包含一些项目信息或链接到其他重要页面。


