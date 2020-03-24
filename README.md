[toc]

#  一．绪论 

## （一）选题背景

​		微博（Weibo）是指一种基于用户关系信息分享、传播以及获取的通过关注机制分享简短实时信息的广播式的社交媒体、网络平台，用户可以通过PC、手机等多种移动终端接入，以文字、图片、视频等多媒体形式，实现信息的即时分享、传播互动，是随着Web 2.0而兴起的一类开放的互联网社交服务。

​		目前国内外无数优秀的微博系统开始涌现。它们允许用户以简短文字随时随地更新自己的状态，每条信息的长度都在140字以内，支持图片、音频、视频等多媒体的出版，每个用户既是微内容的创造者也是微内容的传播者和分享者，极大得拉低了用户的创作门槛，这140字的内容，让每个人都成了莎士比亚。

## （二）选题意义

​		随着计算机技术的飞速发展，大数据时代已经到来，越来越多的移动端应用开始瞄准了用户的碎片化时间（手机游戏，短视频应用等），微博的出现尤其影响了人们的日常社交方式。

​		因此，微博系统的重要性不言而喻，一个稳定，高效，安全的微博系统，方便了用户的社交，加深了用户的交流，保护了用户的隐私，还优化了从发布内容到浏览信息的所有细节，降低了用户的上手操作门槛，拉近了每一个用户之间的距离。

## （三）开发环境

1. 开发所用设备和软件

+ **硬件**

    **MacBook Pro (13-inch, 2018)**

    > **系统** macOS Catalina 10.15.3
    >
    > **CPU** 2.3 GHz 四核Intel Core i5
    >
    > **内存** 8 GB 2133 MHz LPDDR3
    >
    > **磁盘** Macintosh HD

    **腾讯云主机 (标准型S2 1Mbps)**

    >**系统** Ubuntu 16.04.1 LTS
    >
    >**CPU** 1核 
    >
    >**内存** 2GB
    >
    >**磁盘** 高性能云硬盘

+ **软件**

  > **JDK** 1.8.0_231
  >
  > **Tomcat** 8.5.50
  >
  > **MySQL** 5.7
  >
  > **IntelliJ IDEA** 2019.3.2
  >
  > **Navicat Premium** 15.0.8
  >
  > **Spring** 4.2.23
  >
  > **MyBatis** 3.3.0

  

1. 执行与构建

项目基于SpringMVC和Maven构建

在 Ubuntu 16.04.1 LTS 下的基于 JDK 1.8.0_231 的 Tomcat 8.5.50 执行

## （四）技术路线

1. 技术栈

+ 后端
    + Java
    + Spring
    + SpringMVC
    + Tomcat
    + MySQL
    + log4J
    + MyBatis
    + Maven
	+ Linux
	+ WebSocket
    + HTTP
    + Git
    
+ 前端
    + HTML5
    + CSS
    + JavaScript
    + Jsp
    + jquery
    + bootstrap

1. 项目依赖==填充内容注释没写==

```xml
<dependency>
    <groupId>com.github.pagehelper</groupId>
    <artifactId>pagehelper</artifactId>
    <version>5.1.4</version>
</dependency>
<dependency>
    <groupId>com.github.jsqlparser</groupId>
    <artifactId>jsqlparser</artifactId>
    <version>0.9.1</version>
</dependency>
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.11</version>
    <scope>test</scope>
</dependency>
<dependency>
    <groupId>org.mockito</groupId>
    <artifactId>mockito-all</artifactId>
    <version>1.9.5</version>
</dependency>
<dependency>
    <groupId>org.apache.commons</groupId>
    <artifactId>commons-lang3</artifactId>
    <version>3.8</version>
</dependency>
<dependency>
    <groupId>org.hamcrest</groupId>
    <artifactId>hamcrest-core</artifactId>
    <version>1.3</version>
</dependency>
<dependency>
    <groupId>org.hibernate</groupId>
    <artifactId>hibernate-validator</artifactId>
    <version>5.4.1.Final</version>
</dependency>


<!-- https://mvnrepository.com/artifact/commons-fileupload/commons-fileupload -->
<dependency>
    <groupId>commons-fileupload</groupId>
    <artifactId>commons-fileupload</artifactId>
    <version>1.3.3</version>
</dependency>

<!-- https://mvnrepository.com/artifact/commons-io/commons-io -->
<dependency>
    <groupId>commons-io</groupId>
    <artifactId>commons-io</artifactId>
    <version>1.3.2</version>
</dependency>

<!-- https://mvnrepository.com/artifact/org.slf4j/slf4j-log4j12 -->

<dependency>
    <groupId>commons-codec</groupId>
    <artifactId>commons-codec</artifactId>
    <version>1.6</version>
</dependency>
<dependency>
    <groupId>net.coobird</groupId>
    <artifactId>thumbnailator</artifactId>
    <version>0.4.7</version>
</dependency>
<dependency>
    <groupId>log4j</groupId>
    <artifactId>log4j</artifactId>
    <version>1.2.12</version>
</dependency>
<dependency>
    <groupId>com.drewnoakes</groupId>
    <artifactId>metadata-extractor</artifactId>
    <version>2.9.1</version>
</dependency>
<dependency>
    <groupId>javax</groupId>
    <artifactId>javaee-api</artifactId>
    <version>7.0</version>
</dependency>
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-web</artifactId>
    <version>4.3.23.RELEASE</version>
</dependency>
<!-- https://mvnrepository.com/artifact/com.mchange.c3p0/com.springsource.com.mchange.v2.c3p0 -->

<!-- https://mvnrepository.com/artifact/com.mchange/c3p0 -->
<dependency>
    <groupId>com.mchange</groupId>
    <artifactId>c3p0</artifactId>
    <version>0.9.5.4</version>
</dependency>
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-webmvc</artifactId>
    <version>4.3.23.RELEASE</version>
</dependency>
<!-- https://mvnrepository.com/artifact/org.springframework/spring-websocket -->
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-websocket</artifactId>
    <version>4.3.23.RELEASE</version>
</dependency>

<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.11</version>
</dependency>
<!--jstl-->
<dependency>
    <groupId>jstl</groupId>
    <artifactId>jstl</artifactId>
    <version>1.2</version>
</dependency>
<dependency>
    <groupId>taglibs</groupId>
    <artifactId>standard</artifactId>
    <version>1.1.2</version>
</dependency>


<!--mybatis-->
<dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis</artifactId>
    <version>3.3.0</version>
</dependency>
<dependency>
    <groupId>org.mybatis</groupId>
    <artifactId>mybatis-spring</artifactId>
    <version>1.2.3</version>
</dependency>
<!-- https://mvnrepository.com/artifact/org.springframework/spring-test -->

<!-- https://mvnrepository.com/artifact/org.springframework/org.springframework.jdbc -->
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-jdbc</artifactId>
    <version>4.3.23.RELEASE</version>
</dependency>
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-test</artifactId>
    <version>4.3.23.RELEASE</version>
</dependency>
<dependency>
    <groupId>junit</groupId>
    <artifactId>junit</artifactId>
    <version>4.12</version>
    <scope>compile</scope>
</dependency>

<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-core</artifactId>
    <!--确保版本与其他spring开头的依赖相同 -->
    <version>4.3.23.RELEASE</version>
</dependency>

<!-- 打包时报错加的https://mvnrepository.com/artifact/javax.activation/activation -->
<dependency>
    <groupId>javax.activation</groupId>
    <artifactId>activation</artifactId>
    <version>1.1</version>
</dependency>
```



1. 项目结构

```
arvinclub-blog
├── README.md
├── blog-model
│   ├── pom.xml
│   ├── src
│   │   ├── main
│   │   │   └── java
│   │   │       └── com
│   │   │           └── arvinclub
│   │   │               └── model
│   │   │                   ├── entity
│   │   │                   │   ├── Blog.java
│   │   │                   │   ├── Comment.java
│   │   │                   │   └── User.java
│   │   │                   └── util
│   │   │                       ├── BASE64DecodedMultipartFile.java
│   │   │                       ├── ImageSizeUtil.java
│   │   │                       ├── MutedException.java
│   │   │                       └── ToolsUtil.java
│   │   └── test
│   │       └── sql.txt
│   └── target
│       ├── arvinclub-blog.jar
│       ├── classes
│       ├── generated-sources
│       ├── maven-archiver  
│       └── maven-status
│        
│        
├── blog-service
│   ├── pom.xml
│   ├── src
│   │   ├── main
│   │   │   ├── java
│   │   │   │   └── com
│   │   │   │       └── arvinclub
│   │   │   │           └── service
│   │   │   │               ├── config
│   │   │   │               │   ├── GetHttpSessionConfigurator.java
│   │   │   │               │   ├── RootConfig.java
│   │   │   │               │   └── WebSocket.java
│   │   │   │               ├── dao
│   │   │   │               │   ├── BlogDao.java
│   │   │   │               │   ├── CommentDao.java
│   │   │   │               │   └── UserDao.java
│   │   │   │               └── service
│   │   │   │                   ├── BlogService.java
│   │   │   │                   ├── CommentService.java
│   │   │   │                   ├── UserService.java
│   │   │   │                   └── impl
│   │   │   │                       ├── BlogServiceImpl.java
│   │   │   │                       ├── CommentServiceImpl.java
│   │   │   │                       └── UserServiceImpl.java
│   │   │   └── resources
│   │   │       ├── database.properties
│   │   │       ├── log4j.properties
│   │   │       └── mapper
│   │   │           ├── blogMapper.xml
│   │   │           ├── commentMapper.xml
│   │   │           └── userMapper.xml
│   │   └── test
│   │       └── java
│   │           └── com
│   │               └── arvinclub
│   │                   └── service
│   │                       └── MyTest.java
│   └── target
│       ├── arvinclub-blog.jar
│       ├── classes
│       ├── generated-sources
│       ├── generated-test-sources
│       ├── maven-archiver
│       ├── maven-status
│       ├── surefire-reports
│       └── test-classes
│                  
│        
├── blog-web
│   ├── pom.xml
│   ├── src
│   │   └── main
│   │       ├── java
│   │       │   └── com
│   │       │       └── arvinclub
│   │       │           └── web
│   │       │               ├── config
│   │       │               │   ├── BlogWebAppInitializer.java
│   │       │               │   └── WebConfig.java
│   │       │               ├── controller
│   │       │               │   ├── admin
│   │       │               │   │   └── AdminController.java
│   │       │               │   ├── blog
│   │       │               │   │   ├── BlogsController.java
│   │       │               │   │   └── CommentController.java
│   │       │               │   ├── error
│   │       │               │   │   └── ErrorController.java
│   │       │               │   ├── fun
│   │       │               │   │   ├── PageController.java
│   │       │               │   │   ├── RredirectController.java
│   │       │               │   │   └── SearchController.java
│   │       │               │   ├── other
│   │       │               │   │   └── DownloadController.java
│   │       │               │   └── user
│   │       │               │       ├── AttentionController.java
│   │       │               │       ├── LoginController.java
│   │       │               │       └── RegisteController.java
│   │       │               └── filter
│   │       │                   ├── AdminFilter.java
│   │       │                   ├── CharactorFilter.java
│   │       │                   └── userFilter.java
│   │       ├── resources
│   │       │   └── static
│   │       │       ├── assets
│   │       │       │   ├── css
│   │       │       │   ├── fonts
│   │       │       │   ├── images
│   │       │       │   └── js
│   │       │       ├── css
│   │       │       ├── favicon.ico
│   │       │       ├── file
│   │       │       │   └── images
│   │       │       ├── fonts
│   │       │       ├── images
│   │       │       ├── js
│   │       │       ├── lib
│   │       │       │   └── layui
│   │       │       │       ├── css
│   │       │       │       ├── font
│   │       │       │       ├── images
│   │       │       │       ├── lay
│   │       │       ├── prepros-6.config
│   │       │       └── vendor
│   │       │           ├── bootstrap
│   │       │           │   ├── css
│   │       │           │   └── js
│   │       │           └── jquery
│   │       └── webapp
│   │           └── WEB-INF
│   │               ├── admin
│   │               │   └── list.jsp
│   │               ├── attention.jsp
│   │               ├── base.jsp
│   │               ├── blogs.jsp
│   │               ├── chat.jsp
│   │               ├── detail.jsp
│   │               ├── error.jsp
│   │               ├── list.jsp
│   │               ├── login.jsp
│   │               ├── page.jsp
│   │               ├── registe.jsp
│   │               └── search.jsp
│   └── target
│       ├── blog
│       │   ├── META-INF
│       │   └── WEB-INF
│       ├── blog.war
│       ├── classes
│       ├── generated-sources
│       └── maven-archiver
│          
│               
│                
│                      
└── pom.xml
```



## （五）开发设备

**MacBook Pro (13-inch, 2018)**

> macOS Catalina 10.15.3
>
> 2.3 GHz 四核Intel Core i5
>
> 8 GB 2133 MHz LPDDR3
>
> Intel Iris Plus Graphics 655 1536 MB

**腾讯云主机 (标准型S2)**

>Ubuntu 16.04.1 LTS
>
>1核 2GB 1Mbps
>
>系统盘：高性能云硬盘

## （六）主要研究内容

微博系统设计，保证一个高可用的微博网络社交平台

==填充内容==



# 二．开发技术介绍



## （一）Maven简介

1. 历史

   [Maven](https://baike.baidu.com/item/Maven)项目对象模型(POM)，可以通过一小段描述信息来管理项目的构建，报告和文档的[项目管理工具](https://baike.baidu.com/item/项目管理工具/6854630)软件。

   Maven 除了以程序构建能力为特色之外，还提供高级项目管理工具。由于 Maven 的缺省构建规则有较高的可重用性，所以常常用两三行 Maven 构建脚本就可以构建简单的项目。由于 Maven 的面向项目的方法，许多 Apache Jakarta 项目发文时使用 Maven，而且公司项目采用 Maven 的比例在持续增长。

   Maven设计之初， 是为了简化Jakarta Turbine项目的建设。 在几个项目， 每个项目包含了不同的Ant构建文件。 JAR检查到CVS。 Apache组织开发Maven可以建立多个项目， 发布项目信息， 项目部署， 在几个项目中JAR文件提供团队合作和帮助。

   Maven的经历了Maven-> Maven2 -> Maven3的发展

2. 国内外现状

   国内外都有无数知名项目通过maven构建，并托管在GitHub平台

   

## （二）Spring简介

1. 历史

2002 年 10 月，Rod Johnson 撰写了一本名为 Expert One-on-One J2EE 设计和开发的书。本书由 Wrox出版，介绍了当时 Java 企业应用程序开发的情况，并指出了 Java EE 和 EJB 组件框架中的存在的一些主要缺陷。在这本书中，他提出了一个基于普通 Java 类和依赖注入的更简单的解决方案。

在本书发布后不久，开发者 Juergen Hoeller 和 Yann Caroff 说服 Rod Johnson 创建一个基于基础结构代码的开源项目。Rod，Juergen 和 Yann 于 2003 年 2 月左右开始合作开发该项目 。Yann 为新框架创造了“Spring”的名字。Yann Caroff 在早期离开了团队，Rod Johnson 在 2012 年离开，Juergen Hoeller 仍然是 Spring 开发团队的积极成员。

自 2004 年 1.0 版本发布以来，Spring 框架迅速发展。Spring 2.0 于 2006 年 10 月发布，到那时，Spring的下载量超过了 100 万。Spring 2.0 具有可扩展的 XML 配置功能，用于简化 XML 配置，支持 Java 5，额外的 IoC 容器扩展点，支持动态语言。

在 Rod 领导下管理 Interface21 项目于 2007 年 11 月更名为 SpringSource。同时发布了 Spring 2.5。Spring 2.5 中的主要新功能包括支持 Java 6 / Java EE 5，支持注释配置，classpath 中的组件自动检测和兼容 OSGi 的 bundle。

2007 年，SpringSource 从基准资本获得了 A 轮融资（1000万美元）。SpringSource 在此期间收购了多家公司，如Hyperic，G2One 等。2009年8月，SpringSource 以 4.2 亿美元被 VMWare 收购。SpringSource 在几周内收购了云代工厂，这是一家云 PaaS 提供商。2015 年，云代工厂转型成了非营利云代工厂。

2009 年 12 月，Spring 3.0 发布。Spring 3.0 具有许多重要特性，如重组模块系统，支持 Spring 表达式语言，基于 Java 的 bean 配置（JavaConfig），支持嵌入式数据库（如 HSQL，H2 和 Derby），模型验证/ REST 支持和对 Java EE 的支持。

2011 年和 2012 年发布了许多 3.x 系列的小版本。2012 年 7 月，Rod Johnson 离开了团队。2013 年 4月，VMware 和 EMC 通过 GE 投资创建了一家名为 Pivotal 的合资企业。所有的 Spring 应用项目都转移到了 Pivotal。

2013 年 12 月，Pivotal 宣布发布 Spring 框架 4.0。Spring 4.0 是 Spring 框架的一大进步，它包含了对Java 8 的全面支持，更高的第三方库依赖性（groovy 1.8+，ehcache 2.1+，hibernate 3.6+等），Java EE 7 支持，groovy DSL for bean 定义，对 websockets 的支持以及对泛型类型的支持作为注入 bean 的限定符。

2014 年至 2017 年期间发布了许多 Spring 框架 4.xx 系列版本。

Spring 5.0 GA版本于2017年9月28日发布。Spring 5.0开始支持JDK 8和Java EE 7，同时兼容JDK9。全面支持Servlet 3.1，还引入了一个全新的模块Spring WebFlux用于替代老话的 spring-webmvc；对Kotlin也有了更好的支持。

本项目中使用的版本为Spring 4

Spring 4.x新特性：

Spring 4.x全面支持Java 8.0，支持Lambda表达式的使用，提供了对@Scheduled和@PropertySource重复注解的支持，提供了空指针终结者Optional，对核心容器进行增加：支持泛型的依赖注入、Map的依赖注入、Lazy延迟依赖的注入、List注入、Condition条件注解注入、对CGLib动态代理类进行了增强。

Spring 4.x还支持了基于Groovy DSL的配置，提高Bean配置的灵活性。

Spring 4.x开始，Spring MVC基于Servlet 3.0 开发，并且为了方便Restful开发，引入了新的RestController注解器注解，同时还增加了一个AsyncRestTemplate支持Rest客户端的异步无阻塞请求。

Spring框架为任何类型的部署平台上的基于Java的现代企业应用程序提供了全面的编程和配置模型。

Spring的一个关键元素是在应用程序级别的基础架构支持：Spring专注于企业应用程序的“管道”，以便团队可以专注于应用程序级别的业务逻辑，而不必与特定的部署环境建立不必要的联系。

支持政策和迁移

有关最低要求的信息，有关从较早版本升级的指南以及支持政策，请查看[官方的Spring Framework Wiki页面。](https://github.com/spring-projects/spring-framework/wiki/Spring-Framework-Versions)

特征

- [核心技术](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html)：依赖项注入，事件，资源，i18n，验证，数据绑定，类型转换，SpEL，AOP。
- [测试](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/testing.html)：模拟对象，TestContext框架，Spring MVC测试，`WebTestClient`。
- [数据访问](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/data-access.html)：事务，DAO支持，JDBC，ORM，封送XML。
- [Spring MVC](https://docs.spring.io/spring/docs/current/spring-framework-reference/web.html)和 [Spring WebFlux](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html) Web框架。
- [集成](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/integration.html)：远程处理，JMS，JCA，JMX，电子邮件，任务，调度，缓存。
- [语言](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/languages.html)：Kotlin，Groovy，动态语言。

1. 国内外现状

   国内外都有无数知名Java项目通过maven构建，并托管在GitHub平台

### IOC

本章介绍了控制反转（IoC）原理的Spring框架实现。IoC也称为依赖注入（DI）。在此过程中，对象仅通过构造函数参数，工厂方法的参数或在构造或从工厂方法返回后在对象实例上设置的属性来定义其依赖项（即，与它们一起使用的其他对象） 。然后，容器在创建bean时注入那些依赖项。此过程从根本上讲是通过使用类的直接构造或诸如服务定位器模式之类的机制来控制其依赖项的实例化或位置的bean本身的逆过程（因此称为Control Inversion）。

在`org.springframework.beans`和`org.springframework.context`包是Spring框架的IoC容器的基础。该 [`BeanFactory`](https://docs.spring.io/spring-framework/docs/5.2.4.RELEASE/javadoc-api/org/springframework/beans/factory/BeanFactory.html) 界面提供了一种高级配置机制，能够管理任何类型的对象。 [`ApplicationContext`](https://docs.spring.io/spring-framework/docs/5.2.4.RELEASE/javadoc-api/org/springframework/context/ApplicationContext.html) 是的子接口`BeanFactory`。它增加了：

- 与Spring的AOP功能轻松集成
- 消息资源处理（用于国际化）
- 活动发布
- 应用层特定的上下文，例如`WebApplicationContext` 用于Web应用程序中的。

简而言之，`BeanFactory`提供了配置框架和基本功能，并`ApplicationContext`增加了更多针对企业的功能。该`ApplicationContext`是对一个完整的超集`BeanFactory`，并在Spring的IoC容器的描述本章独占使用。有关使用的详细信息`BeanFactory`，而不是`ApplicationContext,`看到 [的`BeanFactory`](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#beans-beanfactory)。

在Spring中，构成应用程序主干并由Spring IoC容器管理的对象称为bean。Bean是由Spring IoC容器实例化，组装和以其他方式管理的对象。否则，bean仅仅是应用程序中许多对象之一。Bean及其之间的依赖关系反映在容器使用的配置元数据中。

1.2 容器概述

该`org.springframework.context.ApplicationContext`接口代表Spring IoC容器，并负责实例化，配置和组装Bean。容器通过读取配置元数据来获取有关要实例化，配置和组装哪些对象的指令。配置元数据以XML，Java批注或Java代码表示。它使您能够表达组成应用程序的对象以及这些对象之间的丰富相互依赖关系。

`ApplicationContext`Spring提供了该接口的几种实现。在独立应用程序中，通常创建[`ClassPathXmlApplicationContext`](https://docs.spring.io/spring-framework/docs/5.2.4.RELEASE/javadoc-api/org/springframework/context/support/ClassPathXmlApplicationContext.html) 或的实例 [`FileSystemXmlApplicationContext`](https://docs.spring.io/spring-framework/docs/5.2.4.RELEASE/javadoc-api/org/springframework/context/support/FileSystemXmlApplicationContext.html)。尽管XML是定义配置元数据的传统格式，但是您可以通过提供少量XML配置来声明性地启用对这些其他元数据格式的支持，从而指示容器将Java注释或代码用作元数据格式。

在大多数应用场景中，不需要显式的用户代码来实例化一个Spring IoC容器的一个或多个实例。例如，在Web应用程序场景中，应用程序文件中的简单八行（约）样板Web描述符XML `web.xml`通常就足够了（请参阅[Web应用程序的便捷ApplicationContext实例化](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#context-create)）。如果使用 [Spring Tool Suite](https://spring.io/tools/sts)（基于Eclipse的开发环境），则只需单击几次鼠标或击键即可轻松创建此样板配置。

下图显示了Spring的工作原理的高级视图。您的应用程序类与配置元数据结合在一起，因此，在`ApplicationContext`创建和初始化之后，您将拥有一个完全配置且可执行的系统或应用程序。

### AOP

面向方面的编程（AOP）通过提供另一种思考程序结构的方式来补充面向对象的编程（OOP）。OOP中模块化的关键单元是类，而在AOP中模块化是方面。方面使关注点（例如事务管理）的模块化跨越了多个类型和对象。（这种关注在AOP文献中通常被称为“跨领域”关注。）

Spring的关键组件之一是AOP框架。虽然Spring IoC容器不依赖于AOP（这意味着您不需要使用AOP），但AOP是对Spring IoC的补充，以提供功能非常强大的中间件解决方案。

具有AspectJ切入点的Spring AOP

Spring通过使用[基于模式的方法](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#aop-schema)或[@AspectJ批注样式，](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#aop-ataspectj)提供了编写自定义方面的简单而强大的方法 。这两种样式都提供了完全类型化的建议，并使用了AspectJ切入点语言，同时仍然使用Spring AOP进行编织。

本章讨论基于架构和基于@AspectJ的AOP支持。[下一章](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#aop-api)将讨论较低级别的AOP支持。

AOP在Spring Framework中用于：

- 提供声明式企业服务。这种服务最重要的是 [声明式事务管理](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/data-access.html#transaction-declarative)。
- 让用户实现自定义方面，并通过AOP补充其对OOP的使用。

### SpringMVC

Spring Web MVC是基于Servlet API构建的原始Web框架，并且从一开始就已包含在Spring框架中。正式名称“ Spring Web MVC”来自其源模块（[`spring-webmvc`](https://github.com/spring-projects/spring-framework/tree/master/spring-webmvc)）的名称，但它通常被称为“ Spring MVC”。

与Spring Web MVC并行，Spring Framework 5.0引入了一个反应式堆栈Web框架，其名称“ Spring WebFlux”也基于其源模块（[`spring-webflux`](https://github.com/spring-projects/spring-framework/tree/master/spring-webflux)）。本节介绍Spring Web MVC。在[下一节](https://docs.spring.io/spring/docs/current/spring-framework-reference/web-reactive.html#spring-web-reactive) 介绍春季WebFlux。

## （三）Mybatis简介

1. Mybatis简介

MyBatis 是支持定制化[ SQL](https://www.w3cschool.cn/sql/)、存储过程以及高级映射的优秀的持久层框架。MyBatis 避免了几乎所有的 JDBC 代码和手动设置参数以及获取结果集。MyBatis 可以对配置和原生Map使用简单的 XML 或注解，将接口和 Java 的 POJOs(Plain Old Java Objects,普通的 Java对象)映射成数据库中的记录。

MyBatis SQL映射器框架使将关系数据库与面向对象的应用程序一起使用变得更加容易。MyBatis使用XML描述符或注释将对象与存储过程或SQL语句耦合。相对于对象关系映射工具，简单性是MyBatis数据映射器的最大优势。

### **优点：**

- 简单易学：本身就很小且简单。没有任何第三方依赖，最简单安装只要两个jar文件+配置几个sql映射文件易于学习，易于使用，通过文档和源代码，可以比较完全的掌握它的设计思路和实现。
- 灵活：mybatis不会对应用程序或者数据库的现有设计强加任何影响。 sql写在xml里，便于统一管理和优化。通过sql基本上可以实现我们不使用数据访问框架可以实现的所有功能，或许更多。
- 解除sql与程序代码的耦合：通过提供DAL层，将业务逻辑和数据访问逻辑分离，使系统的设计更清晰，更易维护，更易单元测试。sql和代码的分离，提高了可维护性。
- 提供映射标签，支持对象与数据库的orm字段关系映射
- 提供对象关系映射标签，支持对象关系组建维护
- 提供xml标签，支持编写动态sql。

### **缺点：**

- 编写SQL语句时工作量很大，尤其是字段多、关联表多时，更是如此。
- SQL语句依赖于数据库，导致数据库移植性差，不能更换数据库。
- 框架还是比较简陋，功能尚有缺失，虽然简化了数据绑定代码，但是整个底层数据库查询实际还是要自己写的，工作量也比较大，而且不太容易适应快速数据库修改。
- 二级缓存机制不佳

MyBatis的功能架构： 


我们把Mybatis的功能架构分为三层：

1. API接口层：提供给外部使用的接口API，开发人员通过这些本地API来操纵数据库。接口层一接收到调用请求就会调用数据处理层来完成具体的数据处理。
2. 数据处理层：负责具体的SQL查找、SQL解析、SQL执行和执行结果映射处理等。它主要的目的是根据调用的请求完成一次数据库操作。
3. 基础支撑层：负责最基础的功能支撑，包括连接管理、事务管理、配置加载和缓存处理，这些都是共用的东西，将他们抽取出来作为最基础的组件。为上层的数据处理层提供最基础的支撑。


Mybatis的使用

要使用 MyBatis， 只需将 mybatis-x.x.x.jar 文件置于 classpath 中即可。

如果使用 Maven 来构建项目，则需将下面的 dependency 代码置于 pom.xml 文件中：

```xml
<dependency>  
    <groupId>org.mybatis</groupId>  
    <artifactId>mybatis</artifactId>  
    <version>x.x.x</version>
</dependency>
```



## （四）Tomcat简介与搭建

### 简介

Apache Tomcat 支持了Java Servlet，JavaServer Page，Java Expression Language和Java的WebSocket技术的一个开源Web容器。Java Servlet，JavaServer Pages，Java Expression Language和Java WebSocket规范是在[Java Community Process](http://jcp.org/en/introduction/overview)下开发的 。它是一个开源的轻量级Web应用服务器，在中小型系统和并发量小的场合下被普遍使用，是开发和调试Servlet、JSP 程序的首选。

  Tomcat主要组件：服务器Server，服务Service，连接器Connector、容器Container。连接器Connector和容器Container是Tomcat的核心。

一个Container容器和一个或多个Connector组合在一起，加上其他一些支持的组件共同组成一个Service服务，有了Service服务便可以对外提供能力了，但是Service服务的生存需要一个环境，这个环境便是Server，Server组件为Service服务的正常使用提供了生存环境，Server组件可以同时管理一个或多个Service服务。



### 搭建

本项目使用的版本是**Tomcat** 8.5.50（https://tomcat.apache.org/download-80.cgi）

目录结构如下所示

```
tomcat
├── BUILDING.txt
├── CONTRIBUTING.md
├── LICENSE
├── NOTICE
├── README.md
├── RELEASE-NOTES
├── RUNNING.txt
├── bin
│   ├── attachments
│   ├── bootstrap.jar
│   ├── catalina-tasks.xml
│   ├── catalina.sh
│   ├── ciphers.sh
│   ├── commons-daemon-native.tar.gz
│   ├── commons-daemon.jar
│   ├── configtest.sh
│   ├── daemon.sh
│   ├── digest.sh
│   ├── hs_err_pid69993.log
│   ├── logs
│   │   └── logback
│   │       ├── error-2020-01-06.log
│   │       ├── smile_2020-1-6.log
│   │       └── spring_2020-1-6.log
│   ├── logs.log
│   ├── logs.log_2020-01-19.log\ \
│   ├── logs.log_2020-02-02.log\ \
│   ├── setclasspath.sh
│   ├── shutdown.sh
│   ├── startup.sh
│   ├── tomcat-juli.jar
│   ├── tomcat-native.tar.gz
│   ├── tool-wrapper.sh
│   └── version.sh
├── conf
│   ├── Catalina
│   │   └── localhost
│   ├── catalina.policy
│   ├── catalina.properties
│   ├── context.xml
│   ├── jaspic-providers.xml
│   ├── jaspic-providers.xsd
│   ├── logging.properties
│   ├── server.xml
│   ├── tomcat-users.xml
│   ├── tomcat-users.xsd
│   └── web.xml
├── lib
├── logs
├── temp
├── webapps
│   ├── ROOT
│   ├── blog
│   ├── blog.war
│   ├── docs
│   ├── examples
│   ├── host-manager
│   ├── manager
└── work
    └── Catalina
        └── localhost
            ├── ROOT
            ├── blog
            ├── docs
            ├── examples
            ├── host-manager
            └── manager
```

先把Tomcat的目录的读写权限设置好，方便接下来的设置与部署。

在conf/server.xml中配置端口号，初始堆大小，最大堆大小，以及自动热部署功能，并把本项目设置为Tomcat的默认应用

最后把本项目编译好的blog.war拷贝到wepapps下，启动Tomcat：startup.sh

Tomcat会启动JVM，自动扫描wepapps下的项目并解压，把类加载到堆内存中。



## （五）WebSocket简介

​		WebSocket 是 HTML5 开始提供的一种在单个 TCP 连接上进行全双工通讯的协议。

​		WebSocket 使得客户端和服务器之间的数据交换变得更加简单，允许服务端主动向客户端推送数据。在 WebSocket API 中，浏览器和服务器只需要完成一次握手，两者之间就直接可以创建持久性的连接，并进行双向数据传输。

​		在 WebSocket API 中，浏览器和服务器只需要做一个握手的动作，然后，浏览器和服务器之间就形成了一条快速通道。两者之间就直接可以数据互相传送。

​		现在，很多网站为了实现推送技术，所用的技术都是 Ajax 轮询。轮询是在特定的的时间间隔（如每1秒），由浏览器对服务器发出HTTP请求，然后由服务器返回最新的数据给客户端的浏览器。这种传统的模式带来很明显的缺点，即浏览器需要不断的向服务器发出请求，然而HTTP请求可能包含较长的头部，其中真正有效的数据可能只是很小的一部分，显然这样会浪费很多的带宽等资源。

​		HTML5 定义的 WebSocket 协议，能更好的节省服务器资源和带宽，并且能够更实时地进行通讯。

​		浏览器通过 JavaScript 向服务器发出建立 WebSocket 连接的请求，连接建立以后，客户端和服务器端就可以通过 TCP 连接直接交换数据。

​		当你获取 Web Socket 连接后，你可以通过 **send()** 方法来向服务器发送数据，并通过 **onmessage** 事件来接收服务器返回的数据。

​		WebSocket 协议本质上是一个基于 TCP 的协议。

​		为了建立一个 WebSocket 连接，客户端浏览器首先要向服务器发起一个 HTTP 请求，这个请求和通常的 HTTP 请求不同，包含了一些附加头信息，其中附加头信息"Upgrade: WebSocket"表明这是一个申请协议升级的 HTTP 请求，服务器端解析这些附加的头信息然后产生应答信息返回给客户端，客户端和服务器端的 WebSocket 连接就建立起来了，双方就可以通过这个连接通道自由的传递信息，并且这个连接会持续存在直到客户端或者服务器端的某一方主动的关闭连接。



## （六）JavaWeb原理介绍



### 简介

Java Web 是用 Java 技术来解决相关 web 互联网领域的技术总和。
Web 包括：web 服务器和 web 客户端两部分。
Java 在客户端的应用有 java applet，使用得很少，Java 在服务器端的应用非常丰富，比如 Servlet，JSP 和第三方框架等等。

1. C/S 体系结构
    （1）概念

  ​			C/S 是 Client/Server 的缩写，即客户端 / 服务器结构。

  	（2）特点

  			这种结构可以充分利用两端硬件环境的优势，将任务合理分配到客户端和服务器，从而降低了系统的通信		开销。同时安全性较高。

3. B/S 体系结构
    （1）概念

  ​		B/S 是 Browser/Server 的缩写，即 浏览器/ 服务器结构。统一采用如 IE、Firefox、Chrome 等浏览器，通过 Web 浏览器向 Web 服务器发送请求，由 Web 服务器进行处理，并将处理结果逐级传回客户端。

​		（2）特点

​				节约了开发成本，是一种全新的软件体系结构。这种体系结构已经成为当今应用软件的首选体系结构。		安全性相对C/S较低。



### Servlet

​		类路径：`javax.servlet.HttpServlet`

​		Servlet是一种独立于平台和协议的服务器端的Java应用程序，可以生成动态的web页面。它担当Web浏览器或其他http客户程序发出请求、与http服务器上的数据库或应用程序之间交互的中间层。

​		Servlet是用Java编写的Server端程序，它与协议和平台无关。Servlet运行于Java服务器中。

​		Java Servlet可以动态地扩展服务器的能力，并采用请求-响应模式提供Web服务。

​		Servlet是使用Java Servlet应用程序设计接口及相关类和方法的Java程序。它在Web服务器上或应用服务器上运行并扩展了该服务器的能力。Servlet装入Web服务器并在Web服务器内执行。

​		Servlet是以Java技术为基础的服务器端应用程序组件，Servlet的客户端可以提出请求并获得该请求的响应，它可以是任何Java程序、浏览器或任何设备。

​		当Web服务器接收到一个HTTP请求时，它会先判断请求内容——如果是静态网页数据，Web服务器将会自行处理，然后产生响应信息；如果牵涉到动态数据，Web服务器会将请求转交给Servlet容器。此时Servlet容器会找到对应的处理该请求的Servlet实例来处理，结果会送回Web服务器，再由Web服务器传回用户端。

​		针对同一个Servlet，Servlet容器会在第一次收到http请求时建立一个Servlet实例，然后启动一个线程。第二次收到http请求时，Servlet容器无须建立相同的Servlet实例，而是启动第二个线程来服务客户端请求。所以多线程方式不但可以提高Web应用程序的执行效率，也可以降低Web服务器的系统负担。



### JSP（JavaServer Pages）

​		类路径：`javax.servlet.jsp`

​		JSP和Servlet的本质是一样的，因为JSP最终需要编译成Servlet才能运行，换句话说JSP是生成Servler的草稿文件。

​		JSP就是在HTML中嵌入Java代码，或者使用JSP标签，包括使用用户自定义标签，从而可以动态的提供内容。早起JSP应用比较广泛，一个web应用可以全部由JSP页面组成，只需要少量的JavaBean即可，但是这样导致了JSP职责过于复杂，这是Java EE标准的出现无疑是雪中送炭，因此JSP慢慢发展成单一的表现技术，不再承担业务逻辑组件以及持久层组件的责任。

原理概述：

​		JSP的本质是servlet，当用户指定servlet发送请求时，servlet利用输出流动态生成HTML页面。由于包含大量的HTML标签。静态文本等格式导致servlet的开发效率极低，所有的表现逻辑，包括布局、色彩及图像等，都必须耦合在Java代码中，起静态的部分无需Java程序控制，只有那些需要从数据库读取或者需要动态生成的页面内容才使用Java脚本控制。

因此，JSP页面内容有以下两部分组成：

+ 静态部分：HTML标签

+ 动态部分：Java脚本



# 三．原型设计



## （一）整体架构设计

项目依据MVC架构，数据模型、视图渲染、处理器处理业务逻辑相互分离，低耦合，高内聚。

Maven项目结构

主模块：arvinclub-blog

主模块又分为为三个子模块：

> **blog-model** 负责数据、实体、模型
>
> **blog-service** 封装可复用的、高可用的业务操作
>
> **blog-web** 负责解析视图，进行页面的渲染（SpringMVC直接与这一层交互）

## （二）数据库设计

依据系统功能实现需求，数据库设计如下：

### 用户：

属性：

+ 用户ID：user_id
+ 用户名：user_name
+ 用户密码：user_password
+ 禁言截止日期：user_date
+ 启用状态：status
+ 权限：admin
+ 禁言状态：muted

表设计：

```mysql
CREATE TABLE `user` (
  `user_id` int(11) NOT NULL AUTO_INCREMENT,
  `user_name` varchar(30) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `user_password` varchar(30) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL,
  `user_date` datetime DEFAULT NULL COMMENT '禁言截止日期，muted为1时才有效',
  `status` int(2) NOT NULL DEFAULT '1' COMMENT '1正常，0停用',
  `admin` int(2) NOT NULL DEFAULT '0' COMMENT '管理员权限',
  `muted` int(2) NOT NULL DEFAULT '0' COMMENT '1禁言，0正常',
  PRIMARY KEY (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=56 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci
```

实体类设计：

```java
/**
 * 用户实体类
 */
public class User {

    /**
     * 用于数据库映射
     */
    private int id;
    private int status;//状态 1正常，0停用:无法登录
    private int admin;//权限
    private int muted;//1禁言，0正常
    private Date muteDeadline;//禁言截止时间 muted为1时才有效

    /**
     * 用于前端显示
     */
    private String muteDeadTime;//muteDeadline 面向前端

    /**
     * 其他
     */
    private int fansCount;
    private int idolCount;

    public int getFansCount() {
        return fansCount;
    }

    public void setFansCount(int fansCount) {
        this.fansCount = fansCount;
    }

    public int getIdolCount() {
        return idolCount;
    }

    public void setIdolCount(int idolCount) {
        this.idolCount = idolCount;
    }

    public String getMuteDeadTime() {
        if (muteDeadTime == null && muteDeadline != null)
            muteDeadTime = ToolsUtil.SIMPLE_DATE_FORMAT.format(muteDeadline);
        return muteDeadTime;
    }

    public void setMuteDeadTime(String muteDeadTime) {
        this.muteDeadTime = muteDeadTime;
    }

    public Date getMuteDeadline() {
        return muteDeadline;
    }

    public void setMuteDeadline(Date muteDeadline) {
        this.muteDeadline = muteDeadline;
    }

    public int getMuted() {
        return muted;
    }

    public void setMuted(int muted) {
        this.muted = muted;
    }

    @NotNull
    @Size(min = 1)
    @Pattern(regexp = "[\\S]+")
    private String name;//用户名

    @NotNull
    @Size(min = 1)
    @Pattern(regexp = "[\\S]+")
    private String password;//密码

    public User() { }

    public User(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public int getAdmin() {
        return admin;
    }

    public void setAdmin(int admin) {
        this.admin = admin;
    }

    public int getStatus() {
        return status;
    }

    public void setStatus(int status) {
        this.status = status;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    @Override
    public String toString() {
        return "{" + id + ":" + name + "}";
    }

    @Override
    public boolean equals(Object o) {
        if (this == o)
            return true;
        if (!(o instanceof User))
            return false;
        User user = (User) o;
        return id == user.getId() || Objects.equals(name, user.getName());
    }

}
```



实体属性图：

<img src="/Users/arvin/Documents/Documents/学校/毕设/images/用户.png" alt="用户" style="zoom:50%;" />

### 博客：

属性：

+ 博客ID：blog_id
+ 博客内容：blog_content
+ 发布时间：blog_time
+ 发布者用户ID：user_id
+ 图片文件名：filenames
+ 状态：status

表设计：

```mysql
CREATE TABLE `blogs` (
  `blog_id` int(11) NOT NULL AUTO_INCREMENT,
  `blog_content` varchar(127) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT '内容',
  `blog_time` datetime DEFAULT NULL COMMENT '发布时间',
  `user_id` int(11) DEFAULT NULL COMMENT '用户',
  `filenames` varchar(510) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT '图片的文件名',
  `status` int(2) NOT NULL DEFAULT '1' COMMENT '1正常，0不展示',
  PRIMARY KEY (`blog_id`),
  KEY `user_id` (`user_id`),
  CONSTRAINT `blogs_ibfk_1` FOREIGN KEY (`user_id`) REFERENCES `user` (`user_id`)
) ENGINE=InnoDB AUTO_INCREMENT=224 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci
```

实体类设计：

```java
/**
 * 博客实体类
 */
public class Blog {
    /**
     * 用于数据库映射
     */
    private int id;
    private String content;//博客内容
    private Date date;//时间，面向数据库
    private User user;//此博客发布者
    private int status;//状态 1显示 0不显示
    private String filenames;//图片文件名，面向数据库
    private List<Comment> commentList;

    /**
     * 用于前端显示
     */
    private String time;//时间，面向前端
    private String[] filenameList;//图片文件名，面向前端

    private int commentCount;
    public void setFilenames(String filenames) {
        this.filenames = filenames;
        if (filenames != null)
            filenameList = filenames.split(" \n ");
    }

    public void setDate(Date date) {
        this.date = date;
    }

    public int getStatus() {
        return status;
    }

    public void setStatus(int status) {
        this.status = status;
    }

    public String[] getFilenameList() {
        return filenameList;
    }

    public String getTime() {
        if (time == null && date != null)
            time = ToolsUtil.SIMPLE_DATE_FORMAT.format(date);
        return time;
    }

    public void setTime(String time) {
        this.time = time;
    }

    public String getFilenames() {
        return filenames;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getContent() {
        return content;
    }

    public void setContent(String content) {
        this.content = content;
    }

    public Date getDate() {
        return date;
    }

    public User getUser() {
        return user;
    }

    public void setUser(User user) {
        this.user = user;
    }

    public List<Comment> getCommentList() {
        return commentList;
    }

    public void setCommentList(List<Comment> commentList) {
        this.commentList = commentList;
    }

    public int getCommentCount() {
        return commentList.size();
    }

    @Override
    public String toString() {
        return id + ":" + content + ":" + ToolsUtil.SIMPLE_DATE_FORMAT.format(date) + "{" + user + "}";
    }

}
```



实体属性图：

<img src="/Users/arvin/Documents/Documents/学校/毕设/images/博客.png" alt="博客" style="zoom:50%;" />

### 评论：

属性：

+ 评论ID：comment_id
+ 所属博客ID：blog_id
+ 评论者用户ID：user_id
+ 评论内容：comment_content
+ 发布评论时间：comment_time
+ 状态：status

表设计：

```mysql
CREATE TABLE `comment` (
  `comment_id` int(11) NOT NULL AUTO_INCREMENT,
  `blog_id` int(11) NOT NULL,
  `user_id` int(11) NOT NULL,
  `comment_content` varchar(127) NOT NULL,
  `comment_time` datetime DEFAULT NULL,
  `status` int(1) NOT NULL DEFAULT '1',
  PRIMARY KEY (`comment_id`)
) ENGINE=InnoDB AUTO_INCREMENT=135 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
```

实体类设计：

```java
/**
 * 评论实体类
 */
public class Comment
{
    /**
     * 用于数据库映射
     */
    private int id;
    private String content;//评论内容
    private Date date;//时间，面向数据库
    private User user;//此评论发布者
    private int status;//状态 1显示 0不显示
    private Blog blog;//对应博客


    /**
     * 用于前端显示
     */
    private String time;//时间，面向前端
    private static final SimpleDateFormat SIMPLE_DATE_FORMAT = new SimpleDateFormat("YYYY年MM月dd日 HH:mm");

    public int getId()
    {
        return id;
    }

    public void setId(int id)
    {
        this.id = id;
    }

    public String getContent()
    {
        return content;
    }

    public void setContent(String content)
    {
        this.content = content;
    }

    public Date getDate()
    {
        return date;
    }

    public void setDate(Date date)
    {
        this.date = date;
        if (date != null)
            time = SIMPLE_DATE_FORMAT.format(date);
    }

    public User getUser()
    {
        return user;
    }

    public void setUser(User user)
    {
        this.user = user;
    }

    public String getTime()
    {
        return time;
    }

    public void setTime(String time)
    {
        this.time = time;
    }

    public int getStatus()
    {
        return status;
    }

    public void setStatus(int status)
    {
        this.status = status;
    }

    public Blog getBlog() {
        return blog;
    }

    public void setBlog(Blog blog) {
        this.blog = blog;
    }

    @Override
    public String toString()
    {
        return "Comment{" +
                "id=" + id +
                ", content='" + content + '\'' +
                ", user=" + user +
                ", time='" + time + '\'' +
                '}';
    }
}
```



实体属性图：

<img src="/Users/arvin/Documents/Documents/学校/毕设/images/评论.png" alt="评论" style="zoom:50%;" />

### 关注：

属性：

+ 关注ID：attention_id
+ 博主用户ID：blogger_id
+ 粉丝用户ID：fans_id
+ 状态：status

表设计：

```mysql
CREATE TABLE `attention` (
  `attention_id` int(11) NOT NULL AUTO_INCREMENT,
  `blogger_id` int(11) NOT NULL,
  `fans_id` int(11) NOT NULL,
  `status` int(1) NOT NULL DEFAULT '1',
  PRIMARY KEY (`attention_id`)
) ENGINE=InnoDB AUTO_INCREMENT=45 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci
```

实体属性图：

<img src="/Users/arvin/Documents/Documents/学校/毕设/images/关注.png" alt="关注" style="zoom:50%;" />



### 实体关系图

![实体关系图](/Users/arvin/Documents/Documents/学校/毕设/images/实体关系图.png)



## （三）主要内容

1. 设计模型

+ Spring的工厂模式：BeanFactory

+ Spring的代理模式：使用了JDK中的动态代理 ` java.reflect.Proxy`

+ DataSouce的工厂模式：SqlSessionFactory

+ MyBatis的代理模式：面向接口编程，自动生成Mapper的实现

2. 三层架构搭建

+ Controller：控制层，主要用作校验参数，接收参数，传递给service层并且返回结果，Controller层负责具体的业务模块流程的控制，在此层里面要调用Serice层的接口来控制业务流程，控制的配置也同样是在Spring的配置文件里面进行，针对具体的业务流程，会有不同的控制器，我们具体的设计过程中可以将流程进行抽象归纳，设计出可以重复利用的子单元流程模块，这样不仅使程序结构变得清晰，也大大减少了代码量。
+ Service：Service层主要负责业务模块的逻辑应用设计。同样是首先设计接口，再设计其实现的类，接着再Spring的配置文件中配置其实现的关联。这样我们就可以在应用中调用Service接口来进行业务处理。Service层的业务实现，具体要调用到已定义的DAO层的接口，封装Service层的业务逻辑有利于通用的业务逻辑的独立性和重复利用性，程序显得非常简洁。
+ Dao：DAO层主要是做数据持久层的工作，负责与数据库进行联络的一些任务都封装在此，DAO层的设计首先是设计DAO的接口，然后在Spring的配置文件中定义此接口的实现类，然后就可在模块中调用此接口来进行数据业务的处理，而不用关心此接口的具体实现类是哪个类，显得结构非常清晰，DAO层的数据源配置，以及有关数据库连接的参数都在Spring的配置文件中进行配置。

各个层之间只能单向调用，禁止逆向调用。

### 1. 主要功能

-  发布微博
-  浏览微博
-  个人空间
-  粉丝关注
-  多人聊天

### 2. 用户登录

-  除了通过注册来添加用户，管理员也可以添加用户。登录后的用户可以进入并使用本系统。

### 3. 修改密码

-  用户和管理员都可以修改密码。

### 4. 粉丝关注

-  用户可以关注自己喜欢的博主，并能够在关注动态看到他们新发的微博。
-  用户还能在关注列表里看到自己关注的所有博主，也可以随时取消关注。
-  博主也可以在个人空间看到有谁关注了自己。

### 5. 用户管理

-  删除用户: 管理员可以删除普通用户。
-  禁言用户: 使普通用户（永久或期限）禁止在本系统发布任何内容。
-  查询用户: 通过用户名或ID查找用户，并查看他们的所有信息。
-  删除博客: 管理员可以删除任何微博。
-  管理员除了拥有以下功能以外，同时拥有普通用户的所有功能。

### 6. 微博系统

-  发布微博: 用户登录后随时可以发布微博（限制140字，9张图片）。
-  查看微博: 用户可以在首页看到微博，也可以在关注动态看到关注的博主发的微博。
-  编辑微博: 用户只能编辑自己已经发出的微博。
-  删除微博: 普通用户只能删除自己发的微博，而管理员能删除任何微博。

### 7. 用户评论

-  用户可以在博客下面发表评论，修改或删除自己发的评论。

### 8. 多人聊天

-  用户可以在多人聊天室参与聊天，所有进入聊天室的用户都可以实时看到聊天内容。

### 9. 站内搜索

-  用户可以通过关键词索==用户==和微博内容。



# 四．项目实现

## （一）项目结构

1. 设计maven的模块结构和依赖关系

    项目分为三个模块：

    > **blog-model** 负责数据、实体、模型
    >
    > **blog-service** 封装可复用的、高可用的业务操作
    >
    > **blog-web** 负责解析视图，进行页面的渲染（SpringMVC直接与这一层交互）

2. 完成 `SpringMVC`（基于注解）的搭建

    本项目基于 `Web 3.0` 抛弃了基于繁琐的 `web.xml` 的形式的旧版，使用更加方便，快捷，现代 `SpringMVC` 类库中提供的现有类来配置 `DispacherServlet`

    扩展AbstractAnnotationConfigDispatcherServletInitializer类会自动配置DispatcherServlet和Spring应用上下文

```java
/**
 * 继承AbstractAnnotationConfigDispatcherServletInitializer来初始化WEB
 * 扩展AbstractAnnotationConfigDispatcherServletInitializer的任意类都会自动配置DispatcherServlet和Spring应用上下文
 */
public class BlogWebAppInitializer extends AbstractAnnotationConfigDispatcherServletInitializer {

    protected String[] getServletMappings() {
        return new String[]{"/"};
    }

    protected Class<?>[] getRootConfigClasses() {
        return new Class<?>[]{RootConfig.class};
    }

    protected Class<?>[] getServletConfigClasses() {
        return new Class<?>[]{WebConfig.class};
    }

    /**
     * 文件上传的临时路径
     */
    @Override
    protected void customizeRegistration(ServletRegistration.Dynamic registration) {
        registration.setMultipartConfig(new MultipartConfigElement("/arvin/file/images/"));
    }

    /**
     * 这项配置使得当handlerMapping（处理器适配）无法找到合适的handler（处理器时）
     * 会抛出异常，方便我们后序的捕获处理
     */
    @Override
    protected FrameworkServlet createDispatcherServlet(WebApplicationContext servletAppContext) {
        final DispatcherServlet dispatcherServlet = (DispatcherServlet) super.createDispatcherServlet(servletAppContext);
        dispatcherServlet.setThrowExceptionIfNoHandlerFound(true);
        return dispatcherServlet;
    }
}

```



3. 完成三层架构的搭建

   + Controller 

     1. DispacherServlet收到发送的HttpServletRequest，调用HandlerMapping处理器映射器。
2. 处理器映射器找到具体的处理器(可以根据xml配置、注解进行查找)，生成处理器对象及处理器拦截器(如果有则生成)一并返回给DispatcherServlet。
   
     3. DispatcherServlet调用HandlerAdapter处理器适配器。
4. HandlerAdapter经过适配调用具体的处理器(Controller，也叫后端控制器)。
     5. Controller执行完成返回ModelAndView。

     业务模块流程。我经常喜欢用控制视图的跳转来简单形容，但是这个是不全面的，因为他除了控制视图的转换之外，还控制了业务的逻辑，但是，这里的控制业务逻辑不是业务逻辑的实现，而仅仅是一个大的模块，你看到之后，知道它实现了这个业务逻辑，但是怎么实现的，不需要关心，仅仅需要调用service层里的一个方法即可，这样使controller层看起来更加清晰。

     controller层负责具体的业务模块流程的控制，在此层要调用service层的接口来控制业务流程，控制的配置也同样是在Spring的配置文件里进行，针对具体的业务流程，会有不同的控制器。我们具体的设计过程可以将流程进行抽象归纳，设计出可以重复利用的子单元流程模块。这样不仅使程序结构变得清晰，也大大减少了代码量。
     
     ```
     controller
     ├── admin
     │   └── AdminController.java
     ├── blog
     │   ├── BlogsController.java
     │   └── CommentController.java
     ├── error
     │   └── ErrorController.java
     ├── fun
     │   ├── PageController.java
     │   ├── RredirectController.java
     │   └── SearchController.java
     ├── other
     │   └── DownloadController.java
     └── user
         ├── AttentionController.java
         ├── LoginController.java
         └── RegisteController.java
     ```
     
     
     
   + Service
   
     封装了一系列的可复用的业务操作功能
   
     service层主要负责业务模块的应用逻辑应用设计。同样是首先设计接口，再设计其实现类，接着再Sprin
   
     的配置文件中配置其实现的关联。这样我们就可以在应用中调用service接口来进行业务处理。service层
   
     的业务实，具体要调用已经定义的dao层接口，封装service层业务逻辑有利于通用的业务逻辑的独立性和
   
     重复利用性。程序显得非常简洁。
   
     ```
     service
     ├── config
     │   ├── GetHttpSessionConfigurator.java
     │   ├── RootConfig.java
     │   └── WebSocket.java
     ├── dao
     │   ├── BlogDao.java
     │   ├── CommentDao.java
     │   └── UserDao.java
     └── service
         ├── BlogService.java
         ├── CommentService.java
         ├── UserService.java
         └── impl
             ├── BlogServiceImpl.java
             ├── CommentServiceImpl.java
             └── UserServiceImpl.java
     ```
   
     

## （二）数据库持久化

1. Mysql的安装（https://dev.mysql.com/downloads/mysql/）

   本项目安装了MySQL5.7，这个版本比较稳定，而且安全性方面有所增强，同时InnoDB首次支持了全文索引

2. 设置mysql，最大连接时间，编码格式等

   配置MySQL的用户名，这里用的root账户，配置好密码，并设置最长连接时间为8小时。并调整时区为北京时间（与操作系统一致），根据机器性能设置最大并发数量，并把所有编码格式都调整为utf-8mb4（Mysql的utf8编码并不是真正的UTF-8编码，Mysql的utf8最多只支持3个字节，而emoji表情、一些特殊的中文字符则需要4个字节才能存储， 因此才会报错。下面是来自[维基百科的Unicode字符平面映射](https://zh.wikipedia.org/wiki/Unicode字符平面映射)，其中UTF-8编码是U+2528D，属于CJK Unified Ideographs Extension B（中日韩统一表意文字扩充B）字符集的字符，处于第二辅助平面（SIP，表意文字补充平面），最多支持4个字节。而Mysql的utf8编码则属于常见的基本多文种平面（BMP，即Unicode编码范围在0000-FFFF之内）的字符，最多支持3个字节。）

3. 设置默认引擎，缓存配置，以及最大并发量

4. 表设计

   设计主要表的第一个版本：用户，博客，评论，关注

5. 添加测试数据

   手动添加测试数据到数据库

6. 数据库移动到服务器

   用MySQL的dump命令导出blog.sql文件，在Linux云主机上导入初始测试数据

7. 构建MyBatis测试

   写一个简单的MyBatis测试，测试其久化功能是否正常，性能是否足够

## （三）日志

1. Log4j介绍

Apache Log4j 2是Log4j的升级版，对Log4j的前身Log4j 1.x进行了重大改进，并提供了Logback中可用的许多改进，同时解决了Logback体系结构中的一些固有问题。

Log4j的API与实现是分开的，从而使应用程序开发人员可以清楚地了解他们可以使用哪些类和方法，同时确保向前的兼容性。这允许Log4j团队以兼容的方式安全地改进实施。

Log4j API是一个日志外观，可以与Log4j实现一起使用，但是也可以在其他日志实现（例如Logback）之前使用。与SLF4J相比，Log4j API具有多个优点：1. Log4j API支持记录[消息](https://logging.apache.org/log4j/2.x/manual/messages.html)而不只是字符串。2. Log4j API支持lambda表达式。3.与SLF4J相比，Log4j API提供了更多的日志记录方法。4.除了SLF4J支持的“参数化日志记录”格式外，Log4j API还支持使用java.text.MessageFormat语法以及printf样式消息的事件。5. Log4j API提供了LogManager.shutdown（）方法。基础的日志记录实现必须实现Terminable接口才能使该方法生效。6.完全支持标记，日志级别和ThreadContext（aka MDC）之类的其他构造。

Log4j 2包含基于LMAX Disruptor库的下一代异步记录器。在多线程方案中，与Log4j 1.x和Logback相比，异步Logger的吞吐量高18倍，延迟降低了几个数量级。有关详细信息，请参见[异步日志记录性能](https://logging.apache.org/log4j/2.x/manual/async.html#Performance)。否则，Log4j 2明显优于Log4j 1.x，Logback和java.util.logging，尤其是在多线程应用程序中。Log4j 2 API将提供最佳性能，而Log4j 2提供对Log4j 1.2，SLF4J，Commons Logging和java.util.logging（JUL）API的支持。

编码为Log4j 2 API的应用程序始终可以选择使用任何SLF4J兼容库作为其Log4j-to-slf4j适配器的记录器实现。与Logback一样，Log4j 2可以在修改后自动重新加载其配置。与Logback不同，它在进行重新配置时不会丢失日志事件。Log4j 2支持基于上下文数据，标记，正则表达式和Log事件中的其他组件进行过滤。可以指定过滤，以将其应用于所有事件，然后再传递给Logger或当事件通过Appender时。此外，过滤器也可以与Loggers关联。与Logback不同，您可以在任何这些情况下使用通用的Filter类。

在Log4j 2中，可以通过代码或配置轻松定义[自定义日志级别](https://logging.apache.org/log4j/2.x/manual/customloglevels.html)。无需子类化。除了使用Log4j API中的许多日志方法之一之外，还可以使用构建器来构造日志事件。有关更多信息，请参见[Log Builder] [manual / logbuilder.html]。

在稳态日志记录期间，Log4j 2 在独立应用程序中是无[垃圾的](https://logging.apache.org/log4j/2.x/manual/garbagefree.html)，而在Web应用程序中是低垃圾的。这样可以减少垃圾收集器上的压力，并可以提供更好的响应时间性能。

2. 用log4j建立项目日志体系

在类路径下创建log4j.properties，并从官网（https://logging.apache.org/log4j/2.x/）拷贝一份log4j.properties的模板，根据实际要求修改loggers, appenders 和layouts，然后再测试日志在控制台和log文件中是否能够正常输出，磨刀不误砍柴工，日志的配置将大大提升接下来的开发效率。

+ Logger: 日志记录器，日志记录的核心类，用于输出不同日志级别的消息
+ Appender: 日志输出目标，用于指定日志输出的目的地，如控制台、文件等等。
+ Layout: 日志格式化器，用于指定日志按照什么格式输出，是日志输出的格式化器。



## （四）交互界面

### 1. 用户登录

输入网址后自动进入登录页面，未登录用户尝试符合/user/**的请求是，会被UserFilter拦截，重定向到登录页面，做到登录校验拦截器的功能。

```java
/**
 * 未登录拦截
 */
@WebFilter(filterName = "userFilter",urlPatterns = "/user/*")
public class UserFilter implements Filter
{
    public void destroy(){}

    public void doFilter(ServletRequest req, ServletResponse resp, FilterChain chain) throws ServletException, IOException
    {
        if (((HttpServletRequest) req).getSession().getAttribute("user") != null)
            chain.doFilter(req, resp);
        else
            ((HttpServletResponse)resp).sendRedirect("/");
    }

    public void init(FilterConfig config){ }

}
```



用户请求登录时，后台验证账户和密码参数，它们都不为空，且验证正确是才回成功登录，清除上一位用户的搜索记录等残留信息，并在会话（HttpSession）中添加登录的用户信息，以便接下来使用和防止被登录拦截器拦截，如果登录失败，则重定向到登录页面，传递错误信息。

```java
/**
 * 登录功能
 */
@PostMapping({"/", "login.html"})
public String login(@Valid User user, Errors errors, HttpSession session, RedirectAttributes model) {
    /*检查用户名和密码是否为空*/
    if (errors.hasErrors())
        return "login";
    /*检查用户名和密码是否正确*/
    User realUser = userService.checkUser(user);
    if (realUser != null) {
        session.setAttribute("user", realUser);
        /*清除搜索的记录*/
        session.removeAttribute("blogList");
        session.removeAttribute("keyword");
        session.removeAttribute("page");
        return "redirect:user/blogs.html";
    }
    /*通知是否有错误*/
    model.addFlashAttribute("msg", "err");
    return "redirect:/";
}
```

相关SQL语句

```mysql
SELECT user_id, user_name, status, admin, user_date, muted, user_password
FROM user
WHERE user_name = '施航程' AND user_password = '123' and status > 0;
```





### 2. 修改密码

用户在已经登录的状态下可以在个人空间修改自己的密码，修改之前会校验密码是否符合规范（任意长度的非空字符串），不符合会抛出异常，警告用户。

```java
/**
 * 修改密码
 */
@PostMapping("user/changePassword")
public String changePassword(HttpSession session, String password) {
    if (!Pattern.matches("[\\S]+", password))
        throw new IllegalArgumentException("密码格式错误!");
    User user = (User) session.getAttribute("user");
    user.setPassword(password);
    userService.changePassword(user);
    return "redirect:/user/page.html";
}
```

相关SQL语句

```mysql
UPDATE user SET user_password = '123456'
WHERE user_id = 2;
```



### 4. 粉丝关注

-  用户可以关注自己喜欢的博主，并能够在关注动态看到他们新发的微博。
-  用户还能在关注列表里看到自己关注的所有博主，也可以随时取消关注。
-  博主也可以在个人空间看到有谁关注了自己。

```java
/**
 * 用户关注相关
 */
@Controller
public class AttentionController {

    @Resource
    private UserService userService;

    /**
     * 关注
     */
    @PostMapping("user/addAttention/{userId}/{page}")
    public String addAttention(HttpSession session, @PathVariable int userId, @PathVariable String page) {
        User me = (User) session.getAttribute("user");
        int myId = me.getId();
        if (myId != userId && !userService.isAttention(me.getId(), userId))
            userService.addAttention(myId, userId);
        return "redirect:/user/page.html/" + userId + "/" + page;
    }

    /**
     * 取关
     */
    @PostMapping("user/delAttention/{userId}/{page}")
    public String delAttention(HttpSession session, @PathVariable int userId, @PathVariable String page) {
        User me = (User) session.getAttribute("user");
        userService.delAttention(me.getId(), userId);
        return "redirect:/user/page.html/" + userId + "/" + page;
    }

    /**
     * 关注列表
     */
    @GetMapping("user/attentionList/{userId}")
    public String attentionList(@PathVariable int userId, Model model) {
        PageInfo<User> listPage = userService.attentionList(userId);
        model.addAttribute("listPage", listPage);
        model.addAttribute("host", userService.findUserById(userId));
        model.addAttribute("msg", "的关注");
        return "list";
    }

    /**
     * 粉丝列表
     */
    @GetMapping("user/fansList/{userId}")
    public String fansList(@PathVariable int userId, Model model) {
        PageInfo<User> listPage = userService.fansList(userId);
        model.addAttribute("listPage", listPage);
        model.addAttribute("host", userService.findUserById(userId));
        model.addAttribute("msg", "的粉丝");
        return "list";
    }
}
```

相关SQL语句

```xml
<insert id="attention">
    INSERT INTO attention(blogger_id, fans_id)
    VALUES (#{blogger}, #{fans})
</insert>

<delete id="delAttention">
    DELETE
    FROM attention
    WHERE blogger_id = #{blogger}
      AND fans_id = #{fans}
</delete>

<select id="attentionList" resultMap="userMap" parameterType="int">
    select u.user_id, u.user_name, u.status, u.admin, u.user_date, u.muted
    from user u
             inner join attention a on u.user_id = a.blogger_id
    where a.fans_id = #{id}
</select>

<select id="fansList" resultMap="userMap">
    select u.user_id, u.user_name, u.status, u.admin, u.user_date, u.muted
    from user u
             inner join attention a on u.user_id = a.fans_id
    where a.blogger_id = #{id}
</select>
```





### 5. 用户管理

-  删除用户: 管理员可以删除普通用户。
-  禁言用户: 使普通用户（永久或期限）禁止在本系统发布任何内容。
-  查询用户: 通过用户名或ID查找用户，并查看他们的所有信息。
-  删除博客: 管理员可以删除任何微博。
-  管理员除了拥有以下功能以外，同时拥有普通用户的所有功能。

非管理员用户尝试符合/admin/**的请求是，会被AdminFilter拦截，重定向到主页面，做到权限校验拦截器的功能。

```java
/**
 * 未登录拦截
 */
@WebFilter(filterName = "adminFilter",urlPatterns = "/admin/*")
public class AdminFilter implements Filter
{
    public void destroy(){}

    public void doFilter(ServletRequest req, ServletResponse resp, FilterChain chain) throws ServletException, IOException
    {
        User user = (User) ((HttpServletRequest) req).getSession().getAttribute("user");
        if (user != null && user.getAdmin() > 0)
            chain.doFilter(req, resp);
        else
            ((HttpServletResponse)resp).sendRedirect("/user/blogs.html");
    }

    public void init(FilterConfig config){ }

}
```



用户请求登录时，后台会在会话（HttpSession）中添加登录的用户信息时，加入用户的管理员权限信息，以便接下来使用和被登录拦截器验证通过或者拦截，如果验证失败，则重定向到主页面。

```java
/**
 * 管理员相关
 */
@Controller
public class AdminController {

    @Resource
    private UserService userService;

    /**
     * 管理员页面,默认第一页
     */
    @GetMapping("admin/manager.html")
    public String admin(Model model, @RequestParam(required = false) String username) {
        return admin(model, 1, username);
    }

    /**
     * 管理员页面,分页
     */
    @GetMapping("admin/manager.html/{page}")
    public String admin(Model model, @PathVariable int page, @RequestParam(required = false) String username) {
        /*根据页号获取数据*/
        username = StringUtils.isEmpty(username) ? null : username.trim();
        PageInfo<User> userPage = userService.selectAllUser(page, username);
        model.addAttribute("userPage", userPage);
        return "admin/list";
    }

    /**
     * 删除用户
     *
     * @param userId userId
     * @param page page
     */
    @PostMapping("admin/delUser/{userId}/{page}")
    public String delUser(@PathVariable int userId, @PathVariable String page) {
        userService.delUser(userId);
        return "redirect:/admin/manager.html/" + page;
    }

    /**
     * 恢复用户
     *
     * @param userId userId
     * @param pages  page
     */
    @PostMapping("admin/reuseUser/{userId}/{pages}")
    public String reuseUser(@PathVariable int userId, @PathVariable String pages) {
        userService.reuseUser(userId);
        return "redirect:/admin/manager.html/" + pages;
    }

    /**
     * 禁言用户
     *
     * @param userId userId
     * @param days   天数
     * @param pages  pages
     */
    @PostMapping("admin/mute/{userId}/{days}/{pages}")
    public String mute(@PathVariable int userId, @PathVariable int days, @PathVariable String pages) {
        userService.mute(userId, days);
        return "redirect:/admin/manager.html/" + pages;
    }

}
```

相关SQL语句

```xml
<select id="selectAllUser" resultMap="userMap" parameterType="string">
    SELECT user_id, user_name, status, admin, user_password, user_date, muted
    FROM user
    <where>
        <if test="_parameter != null">
            user_id = #{key}
            OR user_name LIKE &quot;%&quot;#{key}&quot;%&quot;
        </if>
    </where>
    ORDER BY user_id
</select>

<update id="delUser" parameterType="int">
    UPDATE user
    SET status = 0
    WHERE user_id = #{id}
</update>

<update id="reuseUser" parameterType="int">
    UPDATE user
    SET status = 1
    WHERE user_id = #{id}
</update>

<update id="mute" parameterType="com.arvinclub.model.entity.User">
    UPDATE user
    SET user_date = #{muteDeadline},
        muted     = #{muted}
    WHERE user_id = #{id};
</update>
```





### 6. 微博系统

-  发布微博: 用户登录后随时可以发布微博（限制140字，9张图片）。

1. 从会话（Http Session）中获取当前用户信息，包括用户ID、用户名。
2. 为传过来的博客实体添加图片文件信息（如果用户发了图片的话）。
3. MyBatis自动生成的SQL语句，并执行。
4. 重定向到博客浏览页面，用户就能看到自己刚刚发布的博客了。

```java
/**
 * 发布博客
 *
 * @param blog  博客
 * @param files 图片文件
 * @return 成功则转到社区主页，否则转到错误提示页面
 */
@PostMapping("user/addBlog")
public String addBlog(Blog blog, HttpSession httpSession, @RequestParam MultipartFile[] files) throws Exception {
    User me = (User) httpSession.getAttribute("user");
    userService.checkMuted(me);
    /*给blog添加filenames（面向数据库的图片文件名）*/
    blog.setFilenames(ToolsUtil.saveIMG(files, CLASSPATH));
    blog.setUser(me);
    /*添加博客*/
    blogService.addBlog(blog);
    return "redirect:/user/blogs.html";
}
```

相关SQL语句

```xml
<insert id="addBlog">
    INSERT INTO blogs (blog_content, blog_time, user_id, filenames)
    VALUES (#{content}, #{time}, #{id}, #{filenames})
</insert>
```



-  查看微博: 用户可以在首页看到微博，也可以在关注动态看到关注的博主发的微博。通过页号，查询出一部分信息，并返回，如果未指定页号则默认第一页，

```java
/**
 * 查看博客（默认第一页）
 */
@GetMapping("user/blogs.html")
public String showBlogs(Model model) {
    return showBlogs(model, 1);
}

/**
 * 查看博客（指定页号）
 *
 * @param page 页号
 */
@GetMapping("user/blogs.html/{page}")
public String showBlogs(Model model, @PathVariable int page) {
    /*根据页号获取数据*/
    PageInfo<Blog> blogPage = blogService.selectAllBlog(page);
    model.addAttribute("blogPage", blogPage);
    return "blogs";
}

/**
 * 查看关注动态（默认第一页）
 */
@GetMapping("user/attention.html")
public String attention(Model model,HttpSession session) {
    return attention(model, 1, session);
}

/**
 * 查看关注动态（指定页号）
 *
 * @param page 页号
 */
@GetMapping("user/attention.html/{page}")
public String attention(Model model, @PathVariable int page,HttpSession session) {
    /*根据页号获取数据*/
    User me = (User) session.getAttribute("user");
    PageInfo<Blog> blogPage = blogService.attentionBlogs(me.getId(), page);
    model.addAttribute("blogPage", blogPage);
    return "attention";
}
```

相关SQL语句

```xml
<select id="selectBlogsByUserId" resultMap="blogMap" parameterType="int">
    SELECT blog_id, blog_content, blog_time, user_id, filenames
    FROM blogs
    <where>
        <if test="_parameter > 0">
            user_id = #{id}
        </if>
        AND status = 1
    </where>
    ORDER BY blog_id DESC
</select>

<select id="attentionBlogs" resultMap="blogMap" parameterType="int">
    SELECT blog_id, blog_content, blog_time, user_id, filenames
    FROM blogs
    WHERE status = 1
      AND user_id IN (SELECT blogger_id FROM attention WHERE fans_id = #{id} and status = 1)
    ORDER BY blog_id DESC
</select>
```



+ 个人主页: 用户可以查看其他用户的个人主页，会显示他的所有博客。通过参数中的用户ID，查找某个用户的博客，如果该用户不存在，则抛出异常。通过页号，查询出一部分信息，并返回，如果未指定页号则默认第一页。

```java
/**
 * 个人主页相关
 */
@Controller
public class PageController {
    @Resource
    private BlogService blogService;

    @Resource
    private UserService userService;

    /**
     * 进入我的个人主页（默认第一页）
     */
    @GetMapping("user/page.html")
    public String seeMe(Model model, HttpSession session) {
        return seeWithPage(0, model, "1", session);
    }

    /**
     * 进入某人个人主页（默认第一页）
     */
    @GetMapping("user/page.html/{userID}")
    public String see(@PathVariable int userID, Model model, HttpSession session) {
        return seeWithPage(userID, model, "1", session);
    }

    /**
     * 进入某人个人主页（指定页号）
     */
    @GetMapping("user/page.html/{userID}/{str}")
    public String seeWithPage(@PathVariable int userID, Model model, @PathVariable String str, HttpSession session) {
        /* 确认用户*/
        User me = (User) session.getAttribute("user");
        User someone = userService.findUserById(userID == 0 ? me.getId() : userID);
        /*确认页号,开始查询*/
        PageInfo<Blog> blogPage = blogService.selectBlogsByUserId(someone.getId(), Integer.parseInt(str));
        /*返回信息*/
        model.addAttribute("blogPage", blogPage);
        model.addAttribute("someone", someone);
        boolean hoster = me.equals(someone);
        model.addAttribute("hoster", hoster);
        if (!hoster)
            model.addAttribute("isAttention", userService.isAttention(me.getId(), someone.getId()));
        return "page";
    }
}

```

相关SQL语句

```xml
<select id="selectBlogsByUserId" resultMap="blogMap" parameterType="int">
    SELECT blog_id, blog_content, blog_time, user_id, filenames
    FROM blogs
    <where>
        <if test="_parameter > 0">
            user_id = #{id}
        </if>
        AND status = 1
    </where>
    ORDER BY blog_id DESC
</select>
```

```mysql
SELECT blog_id, blog_content, blog_time, user_id, filenames
FROM blogs
WHERE user_id = 2 AND status = 1 ORDER BY blog_id DESC
LIMIT 15;
```



-  编辑微博: 用户只能编辑自己已经发出的微博。

1. 获取当前登录的用户。
2. 通过传过来的参数：博客ID确定尝试修改的博客。
3. 获取该博客发布者的用户。
4. 确定当前登录的用户是否有权限更改此博客（当前登录的用户就是发布者，或者权限高于发布者则被判断为有权限）。
5. 无论是否修改成功，都重定向到此博客的详情页面。

```java
/**
 * 编辑博客
 *
 * @return 成功则转到个人主页，否则转到错误提示页面
 */
@PostMapping("user/editBlog")
public String editBlog(Blog blog, HttpSession httpSession) {
    /*如果有编辑权限则删除*/
    User me = (User) httpSession.getAttribute("user");
    userService.checkMuted(me);
    Blog oldBlog = blogService.blogDetail(blog.getId());
    User someone = oldBlog.getUser();
    if (me.equals(someone) || me.getAdmin() > someone.getAdmin()) {
        blog.setContent(blog.getContent().replaceAll("\\\\r\\\\n","\r\n"));
        blogService.editBlog(blog);
    }
    return "redirect:/user/detail.html/" + blog.getId();
}
```

相关SQL语句

```xml
<update id="editBlog" parameterType="com.arvinclub.model.entity.Blog">
    update blogs
    set blog_content = #{content}
    where blog_id = #{id}
</update>
```

```mysql
update blogs set blog_content = '测试'
WHERE blog_id = 223;
```



-  删除微博: 普通用户只能删除自己发的微博，而管理员能删除任何微博。

1. 获取当前登录的用户。
2. 通过传过来的参数：博客ID确定尝试的博客。
3. 获取该博客发布者的用户。
4. 确定当前登录的用户是否有权限删除此博客（当前登录的用户就是发布者，或者权限高于发布者则被判断为有权限）。
5. 无论是否删除成功，都重定向到此博客的详情页面。

```java
/**
 * 删除博客
 *
 * @param blogId blog_id
 * @return 成功则转到个人主页，否则转到错误提示页面
 */
@GetMapping("user/delBlog/{blogId}")
public String delBlog(@PathVariable int blogId, HttpSession httpSession) {
    /*如果有编辑权限则删除*/
    Blog blog = blogService.blogDetail(blogId);
    User me = (User) httpSession.getAttribute("user");
    User someone = blog.getUser();
    if (me.equals(someone) || me.getAdmin() > someone.getAdmin())
        blogService.delBlog(blogId);
    return "redirect:/user/page.html/" + blog.getUser().getId();
}
```

相关SQL语句

删除博客实际上是改变此博客的标志，而非真正删除所有数据

```xml
<update id="delBlog" parameterType="int">
    UPDATE blogs
    SET status = 0
    WHERE blog_id = #{id}
</update>
```

```mysql
UPDATE blogs SET status = 0
WHERE blog_id = 223;
```



### 7. 用户评论

-  用户可以在博客下面发表评论，修改或删除自己发的评论。

```java
/**
 * 评论相关
 */
@Controller
public class CommentController {

    @Resource
    private CommentService commentService;
    @Resource
    private UserService userService;

    /**
     * 发布评论
     *
     * @return 成功则转到微博详情，否则转到错误提示页面
     */
    @PostMapping("user/addComment/{blogId}")
    public String addComment(Comment comment, HttpSession httpSession, @PathVariable int blogId) {
        if (StringUtils.isNotBlank(comment.getContent())) {
            /*构建评论*/
            User me = (User) httpSession.getAttribute("user");
            userService.checkMuted(me);
            comment.setUser(me);
            comment.setTime(ToolsUtil.getNowTimeString());
            Blog blog = new Blog();
            blog.setId(blogId);
            comment.setBlog(blog);
            commentService.addComment(comment);
        }
        /*添加评论*/
        return "redirect:/user/detail.html/" + blogId;
    }

    /**
     * 删除评论
     *
     * @return 成功则转到微博详情，否则转到错误提示页面
     */
    @GetMapping("user/delComment/{commentId}")
    public String delComment(HttpSession httpSession, @PathVariable int commentId) {
        Comment comment = commentService.backCommentById(commentId);
        User me = (User) httpSession.getAttribute("user");
        User someone = comment.getUser();
        User blogger = comment.getBlog().getUser();
        if (me.equals(someone) || me.getAdmin() > someone.getAdmin() ||
                me.equals(blogger) || me.getAdmin() > blogger.getAdmin()) {

            commentService.delComment(commentId);
        }
        return "redirect:/user/detail.html/" + comment.getBlog().getId();
    }

    /**
     * 编辑评论
     *
     * @return 成功则转到微博详情，否则转到错误提示页面
     */
    @PostMapping("user/editComment")
    public String editComment(Comment comment, HttpSession httpSession) {
        Comment oldComment = commentService.backCommentById(comment.getId());
        User me = (User) httpSession.getAttribute("user");
        userService.checkMuted(me);
        if (StringUtils.isNotEmpty(comment.getContent()) && me.equals(oldComment.getUser())) {
            commentService.updateComment(comment);
        }
        return "redirect:/user/detail.html/" + oldComment.getBlog().getId();
    }
}
```

相关SQL语句

```xml
<update id="updateComment" parameterType="com.arvinclub.model.entity.Comment"  useGeneratedKeys="true" keyProperty="id">
    update comment
    set comment_content = #{content}
    where comment_id = #{id}
</update>
<delete id="delComment" parameterType="int">
    DELETE FROM comment
    WHERE comment_id = #{id}
</delete>

<select id="backCommentById" resultMap="commentMap" parameterType="int">
    SELECT comment_id, comment_content, comment_time, user_id, status, blog_id
    FROM comment
    WHERE comment_id = #{id}
      AND status = 1
    ORDER BY comment_id
</select>

<select id="backCommentByBlogId" resultMap="commentMap" parameterType="int">
    SELECT comment_id, comment_content, comment_time, user_id, status, blog_id
    FROM comment
    WHERE blog_id = #{id}
      AND status = 1
    ORDER BY comment_id
</select>

<insert id="addComment">
    INSERT INTO comment(blog_id, user_id, comment_content, comment_time)
    VALUES (#{blog}, #{user}, #{content}, #{time})
</insert>


<resultMap id="commentMap" type="com.arvinclub.model.entity.Comment">
    <id column="comment_id" property="id" jdbcType="INTEGER"/>
    <result column="comment_content" property="content" jdbcType="VARCHAR" javaType="string"/>
    <result column="comment_time" property="date" jdbcType="TIMESTAMP" javaType="java.util.Date"/>
    <result column="status" property="status" jdbcType="INTEGER" javaType="int"/>
    <association property="user" select="com.arvinclub.service.dao.UserDao.backUserById" column="user_id"/>
    <association property="blog" select="com.arvinclub.service.dao.BlogDao.backBlogsById" column="blog_id"/>
</resultMap>
```





### 8. 多人聊天

-  用户可以在多人聊天室参与聊天，所有进入聊天室的用户都可以实时看到聊天内容。

利用了java.util.concurrent包下的并发容器ConcurrentHashMap，和保证原子性的int包装类AtomicInteger，每有一个用户连接，则在在线用户集合：clients:ConcurrentHashMap<String, WebSocket>中添加一个用户信息，包含了用户名与会话。同时同步更新在线人数：onlineCount:AtomicInteger

当用户发送消息时，服务端会接收到消息，并转发给当前登录的所有用户，期间对每个用户单独加锁，既保证了每个用户的会话的同步，又保证了并发性能

用户断开连接时，在线用户集合：clients:ConcurrentHashMap<String, WebSocket>和在线人数：onlineCount:AtomicInteger也会同步更新

为了保证系统的高可用

```java
/**
 * 基于WebSocket的多人聊天室
 */
@ServerEndpoint(value = "/webSocketByTomcat", configurator = GetHttpSessionConfigurator.class)
public class WebSocket {
    /**
     * 聊天室人数
     */
    private static final AtomicInteger onlineCount = new AtomicInteger(0);

    /**
     * 当前聊天室成员
     */
    private static final Map<String, WebSocket> clients = new ConcurrentHashMap<>();

    /**
     * 用户信息
     */
    private Session session;
    private String username;
    private final Object lock = new Object();

    /**
     * 新建连接
     */
    @OnOpen
    public void onOpen(Session session, EndpointConfig config) throws Exception {
        //获取HttpSession，并得到用户名
        HttpSession httpSession = (HttpSession) config.getUserProperties().get(HttpSession.class.getName());
        username = ((User) httpSession.getAttribute("user")).getName();

        //登录冲突提醒
        if (clients.containsKey(username)) {
            //language=HTML
            clients.get(username).sendMessageToMe("<span style=\"color:blue\">你已在其他位置登陆</span>");
            clients.get(username).session.close();
        }

        //该用户进入聊天室
        this.session = session;
        clients.put(username, this);

        //聊天室人数调整，并通知其他用户
        onlineCount.set(clients.size());
        //language=HTML
        sendMessageAll("<span style=\"color:green\">[" + username + "] 进入聊天室, 当前人数: " + getOnlineCount() + "</span>");


    }

    /**
     * 关闭连接
     */
    @OnClose
    public void onClose() throws Exception {

        clients.remove(username);
        onlineCount.set(clients.size());
        //language=HTML
        sendMessageAll("<span style=\"color:red\">[" + username + "] 离开聊天室, 当前人数: " + getOnlineCount() + "</span>");
        if (session != null && session.isOpen()) {
            session.close();
        }

    }

    /**
     * 处理收到的消息
     */
    @OnMessage
    public void onMessage(String message) throws IOException {
        if (message.equalsIgnoreCase("clear!!!"))
            for (WebSocket webSocket : clients.values())
                webSocket.session.close();
        else if (message.equalsIgnoreCase("num!!!")) {
            //language=HTML
            sendMessageToMe("<span style=\"color:blue\">当前人数: " + getOnlineCount() + "</span>");
            for (String u : clients.keySet())
                //language=HTML
                sendMessageToMe("<span style=\"color:blue\">[" + u + "]  </span>");
        } else
            sendMessageAll("[" + username + "]: " + message);
    }

    /**
     * 出错也要保证正常关闭和注销
     */
    @OnError
    public void onError(Throwable error) throws Exception {
        if (session != null && session.isOpen()) {
            session.close();
        }
    }


    /**
     * 广播信息
     */
    private void sendMessageAll(String message) throws IOException {
        for (WebSocket item : clients.values())
            synchronized (item.lock) {
                item.session.getBasicRemote().sendText(message);
            }
    }


    /**
     * 打印出提醒（单人）
     */
    private void sendMessageToMe(String message) throws IOException {
        synchronized (lock) {
            session.getBasicRemote().sendText(message);
        }
    }

    /**
     * 获取当前人数
     */
    public static int getOnlineCount() {
        for (String str : clients.keySet())
            if (!clients.get(str).session.isOpen())
                clients.remove(str);
        return onlineCount.get();
    }

}
```

为了保证服务端可以拿到用户名，需要在握手时获取HTTP会话：HttpSession（不是同一个会话），并把HTTP会话保存到WebSocket上下文的用户配置参数 UserProperties中，以便后续获取。

```java
/**
 * 用于WebSocket连接时获取HttpSession
 */
public class GetHttpSessionConfigurator extends Configurator {

    /**
     * 获取HttpSession并放到UserProperties中
     */
    @Override
    public void modifyHandshake(ServerEndpointConfig sec, HandshakeRequest request, HandshakeResponse response) {
        HttpSession httpSession = (HttpSession) request.getHttpSession();
        sec.getUserProperties().put(HttpSession.class.getName(), httpSession);
    }
}
```



### 9. 站内搜索

+ 用户可以通过关键词索用户和微博内容。

用HTTP会话保存用户的搜索记录，以便用户下次再进入搜索页面时，可以重现上一次搜索的结果

```java
/**
 * 查找内容
 */
@Controller
public class SearchController {
    @Resource
    private BlogService blogService;

    /**
     * 进入查找内容页面
     */
    @GetMapping("user/search.html")
    public String search() {
        return "search";
    }

    /**
     * 按关键词查找内容（默认第一页）
     */
    @PostMapping("user/search.html")
    public String search(@RequestParam String keyword, HttpSession session) {
        session.setAttribute("keyword", keyword);
        return searchByPage(1, session);
    }

    /**
     * 按关键词查找内容（指定页号）
     */
    @GetMapping("user/search.html/{page}")
    public String searchByPage(@PathVariable int page, HttpSession session) {
        /*确认关键词*/
        String keyword = (String) session.getAttribute("keyword");
        if (StringUtils.isBlank(keyword))
            return "redirect:/user/search.html";
        /*开始查询,返回信息*/
        session.setAttribute("blogPage", blogService.selectBlogsByKey(keyword, page));
        return "search";
    }

}
```

相关SQL语句

在SQL查询语句的拼接上，占位符使用了#{}而不是${}，#{}使用了预编译SQL语句的形式，不光有效地提升了SQL语句在重复查询上的性能，还能防止被SQL注入。

```xml
<select id="selectBlogsByKey" resultMap="blogMap" parameterType="string">
    SELECT blog_id, blog_content, blog_time, user_id, filenames
    FROM blogs a INNER JOIN user b USING(user_id)
    <where>
        a.status = 1
        AND blog_content LIKE &quot;%&quot;#{key}&quot;%&quot;
        OR user_name LIKE &quot;%&quot;#{key}&quot;%&quot;
    </where>
    ORDER BY blog_id DESC
</select>
```

```mysql
SELECT blog_id, blog_content, blog_time, user_id, filenames
FROM blogs a
INNER JOIN user b USING(user_id)
WHERE a.status = 1 AND blog_content LIKE "%"'test'"%" OR user_name LIKE "%"'test'"%" ORDER BY blog_id DESC
LIMIT 15;
```





# 五．测试

## （一）测试基本微博发送与查看功能

## （二）测试个人空间

## （三）测试聊天等功能

## （四）测试后台管理等功能

## （五）测试用户注册，登录，注销等功能

## （六）测试评论功能

## （七）上线功能



# 六．打包上传

## （一）打包到服务器

## （二）域名申请与备案

## （三）启动项目

## （四）服务器测试与调试