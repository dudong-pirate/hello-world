# 2016 Interview preparation

标签（空格分隔）： Career 

---
JVM 基础知识

Java I/O 阻塞和非阻塞

网络编程的基础知识

Web 开发中的短地址

Java 集合类 LinkedList 和 ArrayList
LinkedList 链表 增删操作快，查询慢
ArrayList 数组 查询快而稳定 尾部增删快，中间增删慢

数据库 事务隔离等级

理解 Maven POM 依赖关系

极客学院
http://wiki.jikexueyuan.com/project/mybatis-in-action/data-operation.html

当两个线程竞争同一资源时，如果对资源的访问顺序敏感，就称存在**竞态条件**。导致竞态条件发生的代码区称作**临界区**。

允许被多个线程同时执行的代码称作**线程安全的代码**。线程安全的代码不包含竞态条件。

当多个线程同时访问同一个资源，并且其中的一个或者多个线程对这个资源进行了**写操作**，才会产生竞态条件。多个线程同时**读**同一个资源不会产生竞态条件。

Java 中的同步块用 synchronized标记。同步块在Java中是同步在某个对象上。所有同步在一个对象上的同步块在同时只能被一个线程进入并执行操作。所有其他等待进入该同步块的线程将被阻塞，直到执行该同步块中的线程退出。
