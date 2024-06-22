# iCloud

1. 英语自我介绍: [自我介绍](D:\Work\简历\self-introduction.docx)

2. 简历中的项目, 针对简历问一些技术, 项目中遇到什么困难, 怎么解决的, 怎么解决的:

   - 内存泄露: C# 事件订阅未及时注销, 如何发现问题的: 用户报告; 如何定位问题: 监控内存

   - 架构模式: DDD, 分层, 依赖注入控制反转, 面向抽象接口编程

     [简历](D:\Work\简历\中文简历\陈思凡_后端开发工程师.pdf)

3. 解决问题的思路

4. 认为什么样的领导是好领导(en)

   ```
   As an employee, I think the focus is not on what the leader is like, but how we communicate and cooperate with the leader and finish the tasks effiently and on time.
   I think the reason why the leader becomes a leader must have their excellences, so I will actively learn from him.Different kinds of leader have their own personality.
   If he is serious , I will learn his efficient attitude and method of doing things; if he is friendly, I will learn his ability to deal with people and learn how to deal with problems.
   
   作为员工，我觉得重点不在于领导是什么样子，而是我们是怎么与领导沟通，配合并完成工作的。
   我觉得领导之所以成为领导一定有他们的过人之处，所以我会积极向他学习。不同类型的领导有各自的特点.
   如果是严肃的领导，我会学习他严谨高效的做事态度和方法；如果是亲和的领导，我会学习他为人处世的能力和处理问题的方法理论。
   
   ```

5. 说说自己的优点和缺点(en)

   ```
   I can quickly familiarize with the business, for example, I was quickly familiar with the business in charge of my departments and took over the project tasks, during the period of communication and coordination with colleagues in multiple departments, I work responsibly, timely response and solve the problems raised by users, the disadvantage of my personal more indoorsy,do not like to exercise
   
   我可以快速熟悉业务, 比如我工作过的三家公司, 我都很快地熟悉了所在部门负责的业务并接手项目任务, 期间与多部门的同事进行了沟通协调, 工作认真负责, 及时响应并解决用户提出的产品问题,缺点的话我个人比较宅, 不爱锻炼
   ```

6. 目前工作最大的挑战 优点缺点(en): 架构设计, 多部门协调沟通, 业务熟悉

   ```
   The biggest challenge of the current work is that the original code structure is confusing, and the special processing logic is not commented and difficult to understand, 
   In the process of code refactoring, I need to consider these special points to ensure that the new architecture will not affect the business after it goes online. 
   For example, when refactoring the function of modifying the warehousing in / out documents, if the goods of the warehousing in / out have unique codes, I need to decide how to handle them according to the unique code configuration of users,
   If the unique code configuration is strong, the goods of the warehousing in / out need to determine whether they have been processed or not, if the configuration is weak, the goods of the warehousing in / out can continue the process without determining whether they have been processed or not.
   Firstly, I communicated with the corresponding product managers, development engineers and test engineers to understand the role of special points, sort out the overall process, and then communicate the details in detail, 
   After the functional refactoring, unit testing and integration testing were conducted to ensure the process integrity of the new architecture.
   
   目前工作最大的挑战是原有代码结构混乱, 特殊的处理逻辑没有注释, 难以理解, 
   在代码重构的过程中需要考虑到这些特殊点, 以保证新架构上线之后不影响业务, 
   
   比如在重构修改出入库单据的功能时, 如果出入库的商品具有唯一编码, 需要根据用户的唯一编码配置信息来决定如何处理出入库的商品,
    
   唯一编码的配置为强状态时, 出入库的商品需要判断是否已经处理过, 如果为弱状态, 出入库的商品无需判断是否已经处理过即可继续后续的流程, 
   我主要跟对应的产品经理与开发工程师以及测试工程师进行沟通, 首先了解唯一编码的作用, 梳理整体流程, 再详细沟通唯一编码的细节, 
   功能重构之后进行单元测试与集成测试, 确保新架构的流程完整性.
   ```

7. 工作中遇到的难忘的问题

8. k8s查看容器日志的命令

   ```shell
   kubectl logs <pod_name> -n <namespace>
   kubectl logs -f <pod_name> -n <namespace>
   ```

   docker logs命令:

   ```shell
   docker logs [options] container_id
   options:
   -details 显示详细信息
   -f, --follow 跟踪实时日志,会实时滚动
   --since string 显示从某个时间之后的日志
   --tail string 从日志末尾显示多少行日志, 默认all
   -t, --timestamps 显示时间戳
   --until string 显示在某个时间之前的日志
   
   例:
   查看从2022年7月1日至今的最后100行日志
   docker logs -f -t --since="2022-07-01" --tail=100 container_id
   
   docker logs -t --since="2022-07-01" --until="2022-07-05" container_id
   ```

   

9. k8s apply和create命令的区别

   #### kubectl create

   create是创建新资源。这里我们需要注意的是，如果再次运行相同的命令，就会抛出错误，因为资源名称在名称空间中应该是唯一的。

   #### kubectl apply

   使配置在资源上生效。 这里分为两种情况，如下：

   1. 资源本不存在：

      创建新资源。

   2. 资源已存在：

      使配置在已存在的资源上生效（也就是更新资源的配置）。若配置没变化，则对应的资源也不会有什么改变, 显示unchanged

10. 如何编译精简的docker镜像

    使用Bazel构建工具

    [强大的自动化构建工具——Bazel](https://blog.csdn.net/Struggle_PAN/article/details/90602753)

11. dockerfile编写与指令解析

    [Docker之Dockerfile编写与指令解析](https://blog.csdn.net/zhangxg0206/article/details/110450283)

12. docker的容器网络类型-网桥模式实现原理

    [浅析docker容器网桥的实现原理以及docker的四种网络模式和bridge模式的具体原理](http://t.zoukankan.com/goloving-p-15133673.html)

13. iptables四表五链

    [Linux防火墙——iptables(四表五链)](https://blog.csdn.net/qq_44870887/article/details/119412685)

14. k8s写入网络规则

    

15. redis分布式锁, 服务a有一个分布式锁, 过期了如何给服务b

    [Redis 分布式锁过期了，但业务还没有执行完，怎么办](https://blog.csdn.net/qq_36594703/article/details/123500652)

16. redis并发竞争key

    [Redis系列教程(七)：Redis并发竞争key的解决方案详解](https://blog.csdn.net/liuhuiteng/article/details/106206494?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-4-106206494-blog-118421144.pc_relevant_aa&spm=1001.2101.3001.4242.3&utm_relevant_index=7)

    [如何解决redis并发竞争key](https://blog.51cto.com/u_15492050/5162443)

17. rabbitmq镜像队列和policy的关系

    [RabbitMQ 镜像队列 使用和原理详解](https://blog.csdn.net/jjhfen00/article/details/124089335)

18. rabbitmq路由模式

19. [RabbitMQ五种工作模式](https://blog.csdn.net/weixin_41882200/article/details/117128590?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_baidulandingword~default-1-117128590-blog-124283720.pc_relevant_aa&spm=1001.2101.3001.4242.2&utm_relevant_index=4)

    [【RabbitMQ】基础四：路由模式（Routing](https://blog.csdn.net/qq_41879343/article/details/111474193)

20. nginx的负载均衡模式

    [nginx负载均衡的常用策略](https://xiaojin21cen.blog.csdn.net/article/details/79903713)

    ![image-20220707122844895](iCloud.assets/image-20220707122844895.png)

21. [kafka和rabbitmq 的区别](https://blog.csdn.net/fwk19840301/article/details/92972814?spm=1001.2101.3001.6650.8&utm_medium=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromBaidu~default-8-92972814-blog-72856762.pc_relevant_aa2&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromBaidu~default-8-92972814-blog-72856762.pc_relevant_aa2&utm_relevant_index=15)

22. [5种避免C＃.NET中因事件造成内存泄漏的方法](https://blog.csdn.net/qq_41872328/article/details/120740922)

23. [可遇不可求的Question之C#中的匿名事件导致内存泄露的解决](http://t.zoukankan.com/tigerjacky-p-2085750.html)

24. [在 C# .NET 中查找、修复和避免内存泄漏](http://www.skcircle.com/?id=1886)