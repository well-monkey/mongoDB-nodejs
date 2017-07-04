**MongoDB+Express 搭建多人博客**

## Express介绍

   express 是 Node.js 上最流行的 Web 开发框架，正如他的名字一样，使用它我们可以快速的开发一个 Web 应用。我们用 express 来搭建我们的博客
    
## MongoDB简介

   MongoDB 是一个基于分布式文件存储的 NoSQL（非关系型数据库）的一种，由 C++ 语言编写，旨在为 WEB 应用提供可扩展的高性能数据存储解决方案。
   
   MongoDB 支持的数据结构非常松散，是类似 json 的 bjson 格式，因此可以存储比较复杂的数据类型。MongoDB 最大的特点是他支持的查询语言非常强大，
   其语法有点类似于面向对象的查询语言，几乎可以实现类似关系数据库单表查询的绝大部分功能，而且还支持对数据建立索引。
   
   MongoDB 没有关系型数据库中行和表的概念，不过有类似的文档和集合的概念。文档是 MongoDB 最基本的单位，每个文档都会以唯一的 _id 标识，
  文档的属性为 key/value 的键值对形式，文档内可以嵌套另一个文档，因此可以存储比较复杂的数据类型。集合是许多文档的总和，一个数据库可以有多个集合，
    一个集合可以有多个文档。
    
    
## 运行项目

 1.安装依赖 cd blog && npm install
 
 2.安装mongoDB 安装完毕
 
      安装 MongoDB 很简单,去 官网 下载对应系统的 MongoDB 即可。
      并在 mongodb 文件夹里新建 blog 文件夹作为我们博客内容的存储目录（非必须）。
      
 3.运行MongoDB：
 
      进入到 bin 目录下：执行命令 mongod --dbpath ../blog/
      
 4.cd blog && supervisor app
 
 5.介绍一些常用的命令
 
    安装express:                       npm install -g express-generator
    建立express博客目录:                express -e blog
    安装依赖:                           cd blog  npm install
    运行: npm start                    默认运行的是 localhost:3000
    bin 目录下运行MongoDB：             mongod --dbpath ../blog/
    使用supervisor命令启动：            npm install -g supervisor
    bin目录下查询MongoDB: 查询用户       mongo    use blog    db.users.find() 
    MongoDB中命令用于删除现有的数据库:    db.dropDatabase()
    查找博客中添加的posts 表里面的内容:   db.getCollection('posts').find({})
 
 6.踩过的坑
       
    很多都是版本号问题，博客内容很多都是老版本的内容，所以在安装的时候最好仔细的看一下具体内容。
    
       "mongodb": "2.2.19",
        
       "body-parser": "~1.17.1",
        
       "cookie-parser": "~1.4.3",
        
       "debug": "~2.6.3",
        
       "ejs": "~2.5.6",
        
       "express": "~4.15.2",
        
       "morgan": "~1.8.1",
        
       "serve-favicon": "~2.4.2",
        
       "express-session": "1.9.1",
        
       "connect-mongo": "0.8.0",
        
       "mongoose ": "~3.8.23"
        

   
    
## 文章推荐

   看过很多关于nodejs+mongodb搭建多人博客的文章，这里像大家推荐一篇相关文章，供大家学习参考。
   
   使用Express与MongoDB 搭建多人博客(http://wiki.jikexueyuan.com/project/express-mongodb-setup-blog/simple-blog.html)
  
## 待完善部分 
    
