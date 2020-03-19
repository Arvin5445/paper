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

1. 项目依赖==注释没写==

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
1. 国内外现状

## （三）Mybatis简介

1. Mybatis简介
2. Mybatis的使用

## （四）Tomcat简介与搭建

## （五）WebSocket简介

## （六）JavaWeb原理介绍



# 三．原型设计

## （一）整体架构设计



## （二）主要内容

1. 设计模型

2. 三层架构搭建



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
   
     封装了一系列的可复用的业务操作业务
   
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

1. Mysql的安装

   本项目安装了MySQL5.7，这个版本比较稳定，而且安全性方面有所增强，同时InnoDB首次支持了全文索引

2. 设置mysql，最大连接时间，编码格式等

   配置MySQL的用户名，这里用的root账户，配置好密码，并设置最长连接时间为8小时。并调整时区为北京时间（与操作系统一致），根据机器性能设置最大并发数量，并把所有编码格式都调整为utf-8mb4（Mysql的utf8编码并不是真正的UTF-8编码，Mysql的utf8最多只支持3个字节，而emoji表情、一些特殊的中文字符则需要4个字节才能存储， 因此才会报错。下面是来自[维基百科的Unicode字符平面映射](https://zh.wikipedia.org/wiki/Unicode字符平面映射)，其中UTF-8编码是U+2528D，属于CJK Unified Ideographs Extension B（中日韩统一表意文字扩充B）字符集的字符，处于第二辅助平面（SIP，表意文字补充平面），最多支持4个字节。而Mysql的utf8编码则属于常见的基本多文种平面（BMP，即Unicode编码范围在0000-FFFF之内）的字符，最多支持3个字节。）

3. 表设计

4. 添加测试数据

5. 数据库移动到服务器

## （三）日志

1. Log4j介绍
2. 用log4j建立项目日志体系

## （四）交互界面

## （五）聊天室的交互实现

## （六）同步聊天室人数



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