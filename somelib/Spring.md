# Spring Framework

AOP (面向方面编程)
IOC(控制反转容器)

Spring 框架的7个模块 如图

* 核心容器 提供Spring 框架的基本功能，主要的组件是BeanFactory 是工程模式的实现 BeanFactory 使用IOC模式将应用程序的配置和依赖性规范与实际的应用程序代码分开
* Spring上下文 Spring 上下文是一个配置文件，向Spring框架提供上下文信息。Spring 上下文包括企业服务，JBDI、DJB、电子邮件、国际化、校验和调度
* Spring AOP 通过配置管理特性，Spring AOP模块直接将面向方面的编程功能集成到了Spring 框架中，所以可以很容易地使Spring框架的任何分支对象支持AOP。Spring AOP模块为基于Spring的应用程序中的对象提供了事务管理服务。通过Spring AOP，不用依赖EJB组件，就可以将声明性事务管理集成到应用程序
* Spring DAO :JDBC DAO 抽象层提供了有意义的异常层次结构，可用该结构来管理异常处理和不同数据库供应商抛出的错误消息。异常层次结构简化了错误处理，并且极大地降低了需要编写的异常代码数量，Spring DAO 的面向JDBC的异常遵从通用的DAO异常层次结构
* Spring ORM :Spring 框架插入了若干个ORM 框架，从而提供了ORM的对象关系工具 其包括JDO、Hibernate和iBatis SQL Map 所有这些都遵从Spring的通用事务和DAO异常层次结构
* Spring Web :Web上下文模块建立在应用程序上下文模块之上，为基于Web的应用程序提供了上下文。所以Spring框架支持与Jakarata Structs 的集成，Web模块还简化了处理多部分请求以及将请求参数绑定到域对象的工作

## IOC 和 AOP

IOC:不创建对象，但是描述创建他们的方式。在代码中不直接与对象和服务连接，但在配置文件中描述哪一个组件需要哪一项服务。容器(在Spring框架中是IOC容器)负责将这些联系在一起

在典型的 IOC 场景中，容器创建了所有对象，并设置必要的属性将它们连接在一起，决定什么时间调用方法。下表列出了 IOC 的一个实现模式。
类型 1	服务需要实现专门的接口，通过接口，由对象提供这些服务，可以从对象查询依赖性（例如，需要的附加服务）
类型 2	通过 JavaBean 的属性（例如 setter 方法）分配依赖性
类型 3	依赖性以构造函数的形式提供，不以 JavaBean 属性的形式公开

Spring 框架的 IOC 容器采用类型 2 和类型3 实现。

### 面向方面的编程

即AOP 是一种编程技术，它允许程序员对横切赶住点或横切典型职责分界线的行为(例如日志和事务管理进行模块化)。AOP的核心构造是方面，他将那些影响多个类的行为封装到可重用的模块中

AOP是IOC补充性的技术，他们都运用模块化的方式解决企业应用程序开发中的复杂问题。在典型的面向对象开发方式中，可能要将日志记录语句放在所有方法和Java类中才能实现日志功能。在AOP方式中，可以反过来将日志服务模块化，并以声明的方式将他们应用到需要日志的组件上，所以Spring AOP编写的应用程序代码是松散耦合的

AOP的功能完全集成到Spring 事务管理、日志和其他各种特性的上下文中

## IOC容器



