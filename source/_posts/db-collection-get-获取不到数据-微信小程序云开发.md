---
title: db.collection.get()获取不到数据---微信小程序云开发
type: article
tags: 常见问题
categories: 微信小程序
cover: https://img-blog.csdnimg.cn/2020070211561671.png
abbrlink: 2126508159
date: 2020-07-02 15:29:07
---
<!-- 解决图片403 -->
<meta name="referrer" content="no-referrer" />

#### 代码：
```js
// 从in_theaters云数据库里获取三条数据
let res = await db.collection("in_theaters").where({}).limit(3).get()
console.log('res=>',res)
```
#### 运行结果：获取不到数据库数据
![图片](https://img-blog.csdnimg.cn/2020070211561671.png)

#### **解决**：修改数据库权限
![图片](https://img-blog.csdnimg.cn/20200702115807699.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3RjMTE0MzQ4MTk1Ng==,size_16,color_FFFFFF,t_70)
#### 改完权限之后运行：成功拿到
![图片](https://img-blog.csdnimg.cn/20200702115929564.png)
