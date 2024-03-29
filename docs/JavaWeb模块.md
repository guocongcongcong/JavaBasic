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

> 所谓"作用域"就是"信息共享的范围"，也就是说一个信息能够在多大的范围内有效.

> JSP的四种范围，分别为page,request,session,application。Web交互的最基本单位为HTTP请求。每个用户从进入网站到离开网站这段过程称为一个HTTP会话，一个服务器的运行过程中会有多个用户访问，就是多个HTTP会话。

> application：服务器启动到停止这段时间。
> session：HTTP会话开始到结束这段时间。
> request：HTTP请求开始到结束这段时间。
> page：当前页面从打开到关闭这段时间。

---

1. application：服务器启动到停止这段时间。Application 的作用范围在服务器一开始执行服务，到服务器关闭为止Application 的范围最、停留的时间也最久，所以使用时要特别注意不然可能会造成服务器负载越来越重的情况。只要将数据存入application对象，数据的范围范围 (Scope) 就为Application ；
> application作用域上的信息传递是通过ServletContext实现的，它提供的主要方法如下所示：
   - Object getAttribute（String name）：从application中获取信息。
   - void setAttribute（String name, Object value）：向application作用域中设置信息。

2. session：HTTP会话开始到结束这段时间。Session 的作用范围为一段用户持续和服务器所连接的时间，但与服务 器断线 ，这个属性就无效。只要将数据存入session对象，数据的范围就为Session；
> session是通过HttpSession接口实现的，它提供的主要方法如下所示:
   - Object HttpSession.getAttribute（String name）：从session中获取信息。
   - void HttpSession.setAttribute（String name, Object value）：向session中保存信息。
   - HttpSession HttpServletRequest.getSessio()：获取当前请求所在的session的对象。
> session的开始时刻比较容易判断，它从浏览器发出第一个HTTP请求即可认为会话开始。但结束时刻就不好判断了，因为浏览器关闭时并不会通知服务器，所以只能通过如下这种方法判断：如果一定的时间内客户端没有反应，则认为会话结束。Tomcat的默认值为120分钟，但这个值也可以通过HttpSession的setMaxInactiveInterval()方法来设置.

3. request：HTTP请求开始到结束这段时间。Request 的范围是指在一JSP 网页发出请求到另一个JSP 网页之间，随 这个属性就失效。设定Request 的范围时可利用request 对象中的setAttribute( )和getAttribute( )；
> 一个HTTP请求的处理可能需要多个Servlet合作，而这几个Servlet之间可以通过某种方式传递信息，但这个信息在请求结束后就无效了。
> Servlet之间的信息共享是通过HttpServletRequest接口的两个方法来实现的。
   - void setAttribute（String name, Object value）：将对象value以name为名称保存到request作用域中。
   - Object getAttribute（String name）：从request作用域中取得指定名字的信息。

JSP中的doGet()、doPost()方法的第一个参数就是HttpServletRequest对象，使用这个对象的 setAttribute()方法即可传递信息。

那么在设置好信息之后，要通过何种方式将信息传给其他的Servlet呢？这就要用到RequestDispatcher接口的forward()方法，通过它将请求转发给其他Servlet。

RequestDispatcher ServletContext.getRequestDispatcher(String path)：取得Dispatcher以便转发。path为转发的目的Servlet。

void RequestDispatcher.forward(ServletRequest request, ServletResponse response)：将request和response转发。

因此，只需要在当前Servlet中先通过setAttribute()方法设置相应的属性，然后使用forward()方法进行跳转，最后在跳转到的Servlet中通过使用getAttribute()方法即可实现信息传递。
 
4. page：当前页面从打开到关闭这段时间。标名pageContext.setAttribute("","");它只能在同一个页面中有效；

> request和page的生命周期都是短暂的，它们之间的区别：一个request可以包含多个page页（include，forward及filter）
为了避免与Servlet API耦合在一起，方便Action类做单元测试，Struts 2对HttpServletRequest、HttpSession和ServletContext进行了封装，构造了三个Map对象来替代这三种对象，在Action中，直接使用HttpServletRequest、HttpSession和ServletContext对应的Map对象来保存和读取数据。
要获取这三个Map对象，可以使用com.opensymphony.xwork2.ActionContext类，ActionContext是action执行的上下文，在ActionContext中保存了action执行所需的一组对象，包括parameters、request、session、application和locale等。ActionContext类定义了如下方法，用于获取HttpServletRequest、HttpSession和ServletContext对应的Map对象。

## 4. session 和 cookie 有什么区别？

1. Cookie是客户端保存用户信息的一种机制，用来记录用户的一些信息，也是实现Session的一种方式|
   Cookies是服务器在本地机器上存储的小段文本并随每一个请求发送至同一个服务器。

2. Session 是在服务端保存的一个数据结构，用来跟踪用户的状态，这个数据可以保存在集群、数据库、文件中；
   session机制是一种服务器端的机制，服务器使用一种类似于散列表的结构（也可能就是使用散列表）来保存信息。


## 5. 说一下 session 的工作原理？

## 6. 如果客户端禁止 cookie 能实现 session 还能用吗？

## 7. spring mvc 和 struts 的区别是什么？

## 8. 如何避免 sql 注入？

## 9. 什么是 XSS 攻击,如何避免？

## 10. 什么是 CSRF 攻击,如何避免？
