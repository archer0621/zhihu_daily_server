### 🍉知乎日报后端接口

##### 🍓前端项目链接: [仿知乎日报前端](https://github.com/archer0621/zhihu_daily)

主要实现知乎日报的基础前后端交互操作，使用 `JSON` 作为数据存储，不涉及到数据库，目前不支持CORS跨域请求，请客户端基于Proxy跨域代理实现

##### 项目启动
> npm install

> node .\server.js

##### 🍇服务器返回信息：

+ code： `0` 表示成功，`1` 表示失败
+ codeText：对状态码的描述

##### 🍓 database：存储相关的数据

##### 🥝 static：存储用户上传的头像

##### 💫相关接口描述：

- 获取最新新闻  
  - url：` /news_latest`  
  - method：`GET`
- 获取以往新闻  
  - url：` /news_before`  
  - method：`GET`
  - params：`time:昨日时间`
- 获取新闻详细信息 
  - url：` /news_info`  
  - method：`GET`
  - params：`id:新闻ID`
- 获取新闻点赞信息 
  - url：` /story_extra`  
  - method：`GET`
  - params：`id:新闻ID`
- 用户登录 
  - url：` /login`  
  - method：`POST`
  - params：`phone: 手机号码, code: 短信验证码`
- 获取手机验证码
  - url：`  /phone_code `  
  - method：`POST`
  - parmas：`phone:手机号`
  - 生成的验证码可在code.txt中查看
- 获取登录者信息
  - url：`  /user_info `  
  - method：`GET`
- 上传图片
  - url：`  /upload `  
  - method：`POST`
  - params：`file:用户头像`
- 修改用户信息
  - url：`  /user_update `  
  - method：`POST`
  - params：`username:用户名, pic：用户头像`
- 收藏新闻
  - url：`  /store `  
  - method：`POST`
  - params：`newsId:新闻ID`
- 取消收藏新闻
  - url：`  /store_remove `  
  - method：`GET`
  - params：`id:收藏ID`
- 获取用户收藏列表
  - url：`  /store_list  `  
  - method：`GET`
  - params：`id:用户ID`

