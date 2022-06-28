# Spring入门

## 一、spring概述

- 非侵入式：基于Spring开发的应用中的对象可以不依赖于Spring的API
- 控制反转：IOC——Inversion of Control，指的是将对象的创建权交给 Spring 去创建。
- 依赖注入：DI—Dependency Injection
- 面向切面编程：Aspect Oriented Programming——AOP
- 容器：Spring 是一个容器，因为它包含并且管理应用对象的生命周期
- 组件化：Spring 实现了使用简单的组件配置组合成一个复杂的应用。在 Spring 中可以使用XML和Java注解组合这些对象。
- 一站式：在 IOC 和 AOP 的基础上可以整合各种企业应用的开源框架和优秀的第三方类库（实际上 Spring 自身也提供了表现层的 SpringMVC 和持久层的 Spring JDBC）。

### **Spring 框架具有以下几个特点：**

##### 1）方便解耦，简化开发

Spring 就是一个大工厂，可以将所有对象的创建和依赖关系的维护交给 Spring 管理。

##### 2）方便集成各种优秀框架

Spring 不排斥各种优秀的开源框架，其内部提供了对各种优秀框架（如 Struts2、Hibernate、MyBatis 等）的直接支持。

##### 3）降低 Java EE API 的使用难度

Spring 对 Java EE 开发中非常难用的一些 API（JDBC、JavaMail、远程调用等）都提供了封装，使这些 API 应用的难度大大降低。

##### 4）方便程序的测试

Spring 支持 JUnit4，可以通过注解方便地测试 Spring 程序。

##### 5）AOP 编程的支持

Spring 提供面向切面编程，可以方便地实现对程序进行权限拦截和运行监控等功能。

##### 6）声明式事务的支持

只需要通过配置就可以完成对事务的管理，而无须手动编程。

## 二、Spring体系结构

![Spring 体系结构](spring.assets/arch1.png)



### 1.Spring core 

核心容器由 **spring-core，spring-beans，spring-context，spring-context-support和spring-expression**组成。

* spring-core提供了框架基本组成部分，包括控制反转和依赖注入。
* spring-beans提供BeanFactory，工程模式的实现。
* context 模块建立在由 core和 beans模块的基础上建立起来的，它以一种类似于 JNDI 注册的方式访问对象。
* spring-expression 模块提供了强大的表达式语言，用于在运行时查询和操作对象图。

### 2.数据集成

数据访问/集成层包括 JDBC，ORM，OXM，JMS 和事务处理模块