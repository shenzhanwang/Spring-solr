# Spring-solr
本项目基于Apache Solr提供一个配置好的搜索引擎并包含一些初始数据，再基于Spring框架连接solr实现企业级搜索的功能。主要内容如下：
1.搜索引擎基于Solr5.3.1，官网：http://lucene.apache.org/solr/
2.Solr中已经配置好三个内核，用于连接三种不同的数据源：
  -moongoDB内核用于同步mongoDB的数据进行搜索；
  -sakila内核用于搜索导入的Mysql中的默认数据库sakila；
  -tika内核用于将本地指定文件夹下的文档（Office或PDF等）导入，进行全文检索。
3.已完成Solr和Tomcat服务器的整合，整个文件夹下载后，进入apache-tomcat-8.0.36中bin目录，双击startup.bat即可开始运行；
4.已整合中文分词器IKAnalyzer，官网https://github.com/EugenePig/ik-analyzer-solr5
5.mongoDB与solr同步工具使用mongo-connector完成，需在Linux下运行，官网https://github.com/mongodb-labs/mongo-connector
6.启动Tomcat后，访问http://localhost:8080/solr/  可进入solr的管理控制台页面，搜索入口访问http://localhost:8080/Spring-solr/search
7.前端暂不提供对sakila和mongoDB的搜索，仅提供了文档的全文检索，要使用数据库的搜索，请进入solr控制台查看效果。
