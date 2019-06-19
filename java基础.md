# JAVA

> 想要面试的初/中/想要面试的初/中/高级 Java 程序员
> 想要查漏补缺的人
> 想要不断完善和扩充自己 Java 技术栈的人
> 原本就掌握了技术却不知道怎么表达的人
> 有上进心,也愿意学习的人

> 面试题覆盖全,且解析全面
> 这份面试题总内容包含了十九个模块：Java 基础、容器、多线程、反射、对象拷贝、Java Web 模块、异常、网络、设计模式、Spring/Spring MVC、Spring Boot/Spring Cloud、Hibernate、Mybatis、RabbitMQ、Kafka、Zookeeper、MySql、Redis、JVM .

- 具体面试题如下:

<!-- TOC depthFrom:2 -->

- [一、 Java 基础](#一-java-基础)
- [二、容器](#二容器)
- [三、多线程](#三多线程)
- [四、反射](#四反射)
- [五、对象拷贝](#五对象拷贝)
- [六、Java Web](#六java-web)
- [七、异常](#七异常)
- [八、网络](#八网络)
- [九、设计模式](#九设计模式)
- [十、Spring/Spring MVC](#十springspring-mvc)
- [十一、Spring Boot/Spring Cloud](#十一spring-bootspring-cloud)
- [十二、Hibernate](#十二hibernate)
- [十三、Mybatis](#十三mybatis)
- [十四、RabbitMQ](#十四rabbitmq)
- [十五、Kafka](#十五kafka)
- [十六、Zookeeper](#十六zookeeper)
- [十七、MySql](#十七mysql)
- [十八、Redis](#十八redis)
- [十九、JVM](#十九jvm)

<!-- /TOC -->

## 一、 Java 基础

1. JDK 和 JRE 有什么区别？
2. == 和 equals 的区别是什么？
3. 两个对象的 hashCode()相同,则 equals()也一定为 true,对吗？
4. final 在 java 中有什么作用？
5. java 中的 Math.round(-1.5) 等于多少？
6. String 属于基础的数据类型吗？
7. java 中操作字符串都有哪些类？它们之间有什么区别？
8. String str="i"与 String str=new String(“i”)一样吗？
9. 如何将字符串反转？
10. String 类的常用方法都有那些？
11. 抽象类必须要有抽象方法吗？
12. 普通类和抽象类有哪些区别？
13. 抽象类能使用 final 修饰吗？
14. 接口和抽象类有什么区别？
15. java 中 IO 流分为几种？
16. BIO、NIO、AIO 有什么区别？
17. Files 的常用方法都有哪些？
18. java 如何解决的多重继承

## 二、容器

1. java 容器都有哪些？
2. Collection 和 Collections 有什么区别？
3. List、Set、Map 之间的区别是什么？
4. HashMap 和 Hashtable 有什么区别？
5. 如何决定使用 HashMap 还是 TreeMap？
6. 说一下 HashMap 的实现原理？
7. 说一下 HashSet 的实现原理？
8. ArrayList 和 LinkedList 的区别是什么？
9. 如何实现数组和 List 之间的转换？
10. ArrayList 和 Vector 的区别是什么？
11. Array 和 ArrayList 有何区别？
12. 在 Queue 中 poll()和 remove()有什么区别？
13. 哪些集合类是线程安全的？
14. 迭代器 Iterator 是什么？
15. Iterator 怎么使用？有什么特点？
16. Iterator 和 ListIterator 有什么区别？
17. 怎么确保一个集合不能被修改？

## 三、多线程

1. 并行和并发有什么区别？
2. 线程和进程的区别？
3. 守护线程是什么？
4. 创建线程有哪几种方式？
5. 说一下 runnable 和 callable 有什么区别？
6. 线程有哪些状态？
7. sleep() 和 wait() 有什么区别
8. 线程的 run()和 start()有什么区别？
9. 创建线程池有哪几种方式？
10. 线程池都有哪些状态？
11. 线程池中 submit()和 execute()方法有什么区别？
12. 在 java 程序中怎么保证多线程的运行安全？
13. 多线程锁的升级原理是什么？
14. 什么是死锁？
15. 怎么防止死锁？
16. ThreadLocal 是什么？有哪些使用场景？
17. 说一下 synchronized 底层实现原理？
18. synchronized 和 volatile 的区别是什么？
19. synchronized 和 Lock 有什么区别？
20. synchronized 和 ReentrantLock 区别是什么？
21. 说一下 atomic 的原理？

## 四、反射

1. 什么是反射？
2. 什么是 java 序列化？什么情况下需要序列化？
3. 动态代理是什么？有哪些应用？
4. 怎么实现动态代理？

## 五、对象拷贝

1. 为什么要使用克隆？
2. 如何实现对象克隆？
3. 深拷贝和浅拷贝区别是什么？

## 六、Java Web

1. jsp 和 servlet 有什么区别？
2. jsp 有哪些内置对象？作用分别是什么？
3. 说一下 jsp 的 4 种作用域？
4. session 和 cookie 有什么区别？
5. 说一下 session 的工作原理？
6. 如果客户端禁止 cookie 能实现 session 还能用吗？
7. spring mvc 和 struts 的区别是什么？
8. 如何避免 sql 注入？
9. 什么是 XSS 攻击,如何避免？
10. 什么是 CSRF 攻击,如何避免？

## 七、异常

> Java 的异常处理是通过 5 个关键字来实现的：try，catch，throw，throws，finally。

1. throw 和 throws 的区别？
2. final、finally、finalize 有什么区别？
3. try-catch-finally 中哪个部分可以省略？
4. try-catch-finally 中,如果 catch 中 return 了,finally 还会执行吗？
5. 常见的异常类有哪些？

## 八、网络

1. http 响应码 301 和 302 代表的是什么？有什么区别？
2. forward 和 redirect 的区别？
3. 简述 tcp 和 udp 的区别？
4. tcp 为什么要三次握手,两次不行吗？为什么？
5. 说一下 tcp 粘包是怎么产生的？
6. OSI 的七层模型都有哪些？
7. get 和 post 请求有哪些区别？
8. 如何实现跨域？
9. 说一下 JSONP 实现原理？

## 九、设计模式

1. 说一下你熟悉的设计模式？
2. 简单工厂和抽象工厂有什么区别？

## 十、Spring/Spring MVC

1. 为什么要使用 spring？
2. 解释一下什么是 aop？
3. 解释一下什么是 ioc？
4. spring 有哪些主要模块？
5. spring 常用的注入方式有哪些？
6. spring 中的 bean 是线程安全的吗？
7. spring 支持几种 bean 的作用域？
8. spring 自动装配 bean 有哪些方式？
9. spring 事务实现方式有哪些？
10. 说一下 spring 的事务隔离？
11. 说一下 spring mvc 运行流程？
12. spring mvc 有哪些组件？
13. @RequestMapping 的作用是什么？
14. @Autowired 的作用是什么？

## 十一、Spring Boot/Spring Cloud

1. 什么是 spring boot？
2. 为什么要用 spring boot？
3. spring boot 核心配置文件是什么？
4. spring boot 配置文件有哪几种类型？它们有什么区别？
5. spring boot 有哪些方式可以实现热部署？
6. jpa 和 hibernate 有什么区别？
7. 什么是 spring cloud？
8. spring cloud 断路器的作用是什么？
9. spring cloud 的核心组件有哪些？

## 十二、Hibernate

1. 为什么要使用 hibernate？
2. 什么是 ORM 框架？
3. hibernate 中如何在控制台查看打印的 sql 语句？
4. hibernate 有几种查询方式？
5. hibernate 实体类可以被定义为 final 吗？
6. 在 hibernate 中使用 Integer 和 int 做映射有什么区别？
7. hibernate 是如何工作的？
8. get()和 load()的区别？
9. 说一下 hibernate 的缓存机制？
10. hibernate 对象有哪些状态？
11. 在 hibernate 中 getCurrentSession 和 openSession 的区别是什么？
12. hibernate 实体类必须要有无参构造函数吗？为什么？

## 十三、Mybatis

1. mybatis 中 #{}和 \${}的区别是什么？
2. mybatis 有几种分页方式？
3. RowBounds 是一次性查询全部结果吗？为什么？
4. mybatis 逻辑分页和物理分页的区别是什么？
5. mybatis 是否支持延迟加载？延迟加载的原理是什么？
6. 说一下 mybatis 的一级缓存和二级缓存？
7. mybatis 和 hibernate 的区别有哪些？
8. mybatis 有哪些执行器(Executor)？
9. mybatis 分页插件的实现原理是什么？
10. mybatis 如何编写一个自定义插件？

## 十四、RabbitMQ

1. rabbitmq 的使用场景有哪些？
2. rabbitmq 有哪些重要的角色？
3. rabbitmq 有哪些重要的组件？
4. rabbitmq 中 vhost 的作用是什么？
5. rabbitmq 的消息是怎么发送的？
6. rabbitmq 怎么保证消息的稳定性？
7. rabbitmq 怎么避免消息丢失？
8. 要保证消息持久化成功的条件有哪些？
9. rabbitmq 持久化有什么缺点？
10. rabbitmq 有几种广播类型？
11. rabbitmq 怎么实现延迟消息队列？
12. rabbitmq 集群有什么用？
13. rabbitmq 节点的类型有哪些？
14. rabbitmq 集群搭建需要注意哪些问题？
15. rabbitmq 每个节点是其他节点的完整拷贝吗？为什么？
16. rabbitmq 集群中唯一一个磁盘节点崩溃了会发生什么情况？
17. rabbitmq 对集群节点停止顺序有要求吗？

## 十五、Kafka

1. kafka 可以脱离 zookeeper 单独使用吗？为什么？
2. kafka 有几种数据保留的策略？
3. kafka 同时设置了 7 天和 10G 清除数据,到第五天的时候消息达到了 10G,这个时候 kafka 将如何处理？
4. 什么情况会导致 kafka 运行变慢？
5. 使用 kafka 集群需要注意什么？

## 十六、Zookeeper

1. zookeeper 是什么？
2. zookeeper 都有哪些功能？
3. zookeeper 有几种部署模式？
4. zookeeper 怎么保证主从节点的状态同步？
5. 集群中为什么要有主节点？
6. 集群中有 3 台服务器,其中一个节点宕机,这个时候 zookeeper 还可以使用吗？
7. 说一下 zookeeper 的通知机制？

## 十七、MySql

1. 数据库的三范式是什么？
2. 一张自增表里面总共有 7 条数据,删除了最后 2 条数据,重启 mysql 数据库,又插入了一条数据,此时 id 是几？
3. 如何获取当前数据库版本？
4. 说一下 ACID 是什么？
5. char 和 varchar 的区别是什么？
6. float 和 double 的区别是什么？
7. mysql 的内连接、左连接、右连接有什么区别？
8. mysql 索引是怎么实现的？
9. 怎么验证 mysql 的索引是否满足需求？
10. 说一下数据库的事务隔离？
11. 说一下 mysql 常用的引擎？
12. 说一下 mysql 的行锁和表锁？
13. 说一下乐观锁和悲观锁？
14. mysql 问题排查都有哪些手段？
15. 如何做 mysql 的性能优化？

## 十八、Redis

1. redis 是什么？都有哪些使用场景？
2. redis 有哪些功能？
3. redis 和 memecache 有什么区别？
4. redis 为什么是单线程的？
5. 什么是缓存穿透？怎么解决？
6. redis 支持的数据类型有哪些？
7. redis 支持的 java 客户端都有哪些？
8. jedis 和 redisson 有哪些区别？
9. 怎么保证缓存和数据库数据的一致性？
10. redis 持久化有几种方式？
    189.redis 怎么实现分布式锁？
11. redis 分布式锁有什么缺陷？
12. redis 如何做内存优化？
13. redis 淘汰策略有哪些？
14. redis 常见的性能问题有哪些？该如何解决？

## 十九、JVM

1. 说一下 jvm 的主要组成部分？及其作用？
2. 说一下 jvm 运行时数据区？
3. 说一下堆栈的区别？
4. 队列和栈是什么？有什么区别？
5. 什么是双亲委派模型？
6. 说一下类加载的执行过程？
7. 怎么判断对象是否可以被回收？
8. java 中都有哪些引用类型？
9. 说一下 jvm 有哪些垃圾回收算法？
10. 说一下 jvm 有哪些垃圾回收器？
11. 详细介绍一下 CMS 垃圾回收器？
12. 新生代垃圾回收器和老生代垃圾回收器都有哪些？有什么区别？
13. 简述分代垃圾回收器是怎么工作的？
14. 说一下 jvm 调优的工具？
15. 常用的 jvm 调优的参数都有哪些？
