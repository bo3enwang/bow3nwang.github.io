---
title: Spring 的基本概念

date: 2018-01-9 22:00:00

categories:
- Java
- Spring

tags:
- Spring

toc: false
thumbnail: 
banner: 

---


2003年2月Spring框架正式称为一道开源项目，Spring致力于J2EE应用的各种解决方案，而不仅仅专注于某一层解决方案。可以说Spring是企业应用开发的“一站式”选择， Spring贯穿于表现层、业务层、持久层，然而Spring并不想取代那些已经有的框架，而是以高度的开放性，与这些已有的框架进行整合。

<!-- more -->

Spring是一个全面的解决方案，它坚持一个原则：不从新造轮子。已经有较好解决方案的领域，Spring绝不重复性实现，比如：对象持久化和OR映射，Spring只对现有的JDBC，Hibernate等技术提供支持，使之更容易使用，而不做重复的实现。Spring框架有很多特性，这些特性由7个定义良好的模块构成。



-  Spring Core：即，Spring核心，它是框架最基础的部分，提供IOC和依赖注入特性
- Spring Context：即，Spring上下文容器，它是BeanFactory功能加强的一个子接口
- Spring Web：它提供Web应用开发的支持
- Spring MVC：它针对Web应用中MVC思想的实现
- Spring DAO：提供对JDBC抽象层，简化了JDBC编码，同时，编码更具有健壮性。
- Spring ORM：它支持用于流行的ORM框架的整合，比如：Spring + Hibernate、Spring + iBatis、Spring + JDO的整合等等。
- Spring AOP：AOP即，面向切面编程，它提供了与AOP联盟兼容的编程实现



本质上 Spring 是对 Java EE 的补足，Spring 并没有完全实现的规范。仅仅小心的选择了一些独立的规范。以下是 Spring 选择的规范，如果需要更深入的理解 Spring 的设计理念，你可以从中找到答案。

- Servlet API ([JSR 340](https://jcp.org/en/jsr/detail?id=340))
- WebSocket API ([JSR 356](https://www.jcp.org/en/jsr/detail?id=356))
- Concurrency Utilities ([JSR 236](https://www.jcp.org/en/jsr/detail?id=236))
- JSON Binding API ([JSR 367](https://jcp.org/en/jsr/detail?id=367))
- Bean Validation ([JSR 303](https://jcp.org/en/jsr/detail?id=303))
- JPA ([JSR 338](https://jcp.org/en/jsr/detail?id=338))
- JMS ([JSR 914](https://jcp.org/en/jsr/detail?id=914))
- Dependency Injection ([JSR 330](https://www.jcp.org/en/jsr/detail?id=330))
- Common Annotations ([JSR 250](https://jcp.org/en/jsr/detail?id=250)) 

