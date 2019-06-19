# Java Web

<!-- TOC -->

- [Java Web](#java-web)
    - [1. jsp 和 servlet 有什么区别？](#1-jsp-和-servlet-有什么区别)
    - [2. jsp 有哪些内置对象？作用分别是什么？](#2-jsp-有哪些内置对象作用分别是什么)
    - [3. 说一下 jsp 的 4 种作用域？](#3-说一下-jsp-的-4-种作用域)
    - [4. session 和 cookie 有什么区别？](#4-session-和-cookie-有什么区别)
    - [5. 说一下 session 的工作原理？](#5-说一下-session-的工作原理)
    - [6. 如果客户端禁止 cookie 能实现 session 还能用吗？](#6-如果客户端禁止-cookie-能实现-session-还能用吗)
    - [7. spring mvc 和 struts 的区别是什么？](#7-spring-mvc-和-struts-的区别是什么)
    - [8. 如何避免 sql 注入？](#8-如何避免-sql-注入)
    - [9. 什么是 XSS 攻击,如何避免？](#9-什么是-xss-攻击如何避免)
    - [10. 什么是 CSRF 攻击,如何避免？](#10-什么是-csrf-攻击如何避免)

<!-- /TOC -->

## 1. jsp 和 servlet 有什么区别？

[link](https://blog.csdn.net/lyhkmm/article/details/78260003)

一. 概念

- Servlet
  - Servlet（Server Applet）是 Java Servlet 的简称，是为小服务程序或服务连接器，用 Java 编写的服务器端程序，主要功能在于交互式地浏览和修改数据，生成动态 Web 内容。
  - 狭义的 Servlet 是指 Java 语言实现的一个接口，广义的 Servlet 是指任何实现了这个 Servlet 接口的类，一般情况下，人们将 Servlet 理解为后者。Servlet 运行于支持 Java 的应用服务器中。从原理上讲，Servlet 可以响应任何类型的请求，但绝大多数情况下 Servlet 只用来扩展基于 HTTP 协议的 Web 服务器。
- JSP
  - JSP 全名为 Java Server Pages，中文名叫 java 服务器页面，其根本是一个简化的 Servlet 设计，它是由 Sun Microsystems 公司倡导. 许多公司参与一起建立的一种动态网页技术标准。JSP 技术有点类似 ASP 技术，它是在传统的网页 HTML（标准通用标记语言的子集）文件(_.htm,_.html)中插入 Java 程序段(Scriptlet)和 JSP 标记(tag)，从而形成 JSP 文件，后缀名为(\*.jsp)。 用 JSP 开发的 Web 应用是跨平台的，既能在 Linux 下运行，也能在其他操作系统上运行。

二. 区别

1. JSP 第一次运行的时候会编译成 Servlet，驻留在内存中以供调用。
2. JSP 是 web 开发技术，Servlet 是服务器端运用的小程序，我们访问一个 JSP 页面时，服务器会将这个 JSP 页面转变成 Servlet 小程序运行得到结果后，反馈给用户端的浏览器。
3. Servlet 相当于一个控制层再去调用相应的 JavaBean 处理数据,最后把结果返回给 JSP。
4. Servlet 主要用于转向，将请求转向到相应的 JSP 页面。
5. JSP 更多的是进行页面显示，Servlet 更多的是处理业务，即 JSP 是页面，Servlet 是实现 JSP 的方法。
6. Servlet 可以实现 JSP 的所有功能，但由于美工使用 Servlet 做界面非常困难，后来开发了 JSP。
7. JSP 技术开发网站的两种模式：JSP + JavaBean；JSP + Servlet + JavaBean（一般在多层应用中, JSP 主要用作表现层,而 Servlet 则用作控制层,因为在
8. JSP 中放太多的代码不利于维护，而把这留给 Servlet 来实现,而大量的重复代码写在 JavaBean 中）

三. 概括
JSP 是 Servlet 技术的扩展，本质上就是 Servlet 的简易方式。JSP 编译后是“类 servlet”。Servlet 和 JSP 最主要的不同点在于，Servlet 的应用逻辑是在 Java 文件中，并且完全从表示层中的 HTML 里分离开来。而 JSP 的情况是 Java 和 HTML 可以组合成一个扩展名为.jsp 的文件。JSP 侧重于视图，Servlet 主要用于控制逻辑。

## 2. jsp 有哪些内置对象？作用分别是什么？

| 对象        | 作用                                                 |
| ----------- | ---------------------------------------------------- |
| request     | 用户端请求，此请求会包含来自  GET/POST  请求的参数； |
| response    | 网页传回用户端的回应；                               |
| pageContext | 网页的属性是在这里管理；                             |
| session     | 与请求有关的会话期；                                 |
| application | servlet  正在执行的内容；                            |
| out         | 用来传送回应的输出；                                 |
| config      | servlet  的构架部件；                                |
| page        | JSP  网页本身；                                      |
| exception   | 针对错误网页，未捕捉的例外。                         |

## 3. 说一下 jsp 的 4 种作用域？

[link](https://blog.csdn.net/qq_36871364/article/details/70153502)


## 4. session 和 cookie 有什么区别？

## 5. 说一下 session 的工作原理？

## 6. 如果客户端禁止 cookie 能实现 session 还能用吗？

## 7. spring mvc 和 struts 的区别是什么？

## 8. 如何避免 sql 注入？

## 9. 什么是 XSS 攻击,如何避免？

## 10. 什么是 CSRF 攻击,如何避免？
