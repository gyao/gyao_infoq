AppDynamics在APM解决方案中添加最终用户监控功能
===

Posted by **[Fabian Lange][1]** on Mar 09, 2012 

   [1]: http://www.infoq.com/author/Fabian-Lange


Application Performance Management Vendor AppDynamics [announced End User Monitoring Support][13] on Tuesday, March 7th. The capability to measure browser rendering times and network latency is added as an integral part to the solution at no extra cost. It seamlessly integrates into existing business transactions and the traffic shows also up on the flow map. 

应用程序性能管理系统（Application Performance Management，APM）提供商AppDynamics于3月7日[宣布推出最终用户监控功能][13]。新功能具备测量浏览器渲染时间和网络延迟能力，作为性能管理解决方案的一部分，用户无需额外付费。该功能无缝集成到现有的业务事物中，并且最终用户流量将会一并显示在流量图表中。

   [13]: http://www.appdynamics.com/blog/2012/03/06/appdynamics-disrupts-apm-market-with-free-end-user-monitoring/

End User Monitoring (EUM) is considered as an essential dimension for APM products by customers and analysts, but whilst other vendors such as [New Relic][14] and [dynaTrace][15] already have these capabilities in their products AppDynamics was only able to monitor Java and .NET application servers until now. All three products use their agents to modify the generated HTML sent back from the monitored systems. The modified HTML includes JavaScript which records page load and render times and sends it back to the APM system. This allows them to monitor the performance perceived by the end user and possibly to fix issues that occur only in specific regions or browsers. 

最终用户监控（EUM）被认为是APM产品的基本功能之一，但与此同时其它APM供应商，如[New Relic][14]和[dynaTrace][15]，已经在他们的产品中提供了上述功能，AppDynamics截至目前只能提供Java和.NET应用程序服务器监控。所有的三个产品都应用他们自己的代理程序来修改被监控系统生成的返回HTML。修改后的HTML包括了用来记录页面加载和渲染时间的JavaScript，并将数据发送回APM系统。这样APM系统就可以监控最终用户感知到的性能，并可以辅助修复只在特定地域或浏览器才发生的问题。

   [14]: http://newrelic.com/features/real-user-monitoring
   [15]: http://www.dynatrace.com/en/solutions-user-experience-management.aspx

Older products on the market, like [BMC Coradiant][16], or [Tivoli ETEWatch][17], used network sniffing technologies to measure network times, but none of them was including the time spent in the browser, which is increasing in importance with dynamic scripting on the browser side. Additionally, those technologies cannot be used to monitor applications hosted in the cloud, like on IaaS or PaaS, as they required addition of a network appliance. 

市场上其它产品，如[BMC Coradiant][16]或[Tivoli ETEWatch][17]，使用网络嗅探技术测量网络耗时，但它们都不能监测浏览器渲染时间，然而现在浏览器端负责执行越来越多的动态脚本，这就让EUM变得愈加重要。此外，这些技术不能用来监测部署在云端，如IaaS或PaaS，上的应用程序，因为这些技术需要额外的网络设备支持。

   [16]: http://www.bmc.com/products/brand/coradiant.html
   [17]: http://www-01.ibm.com/software/tivoli/products/etewatch/

According to AppDynamics, the major differentiators of their approach are their dynamic baselining technique, which is extended to include browser metrics and network latency, and the way the collected data is transferred back to the server. Data is collected by a piece of JavaScript, which is inserted by the agent running in the application server. It collects the data and sends it back with the next regular request, instead of creating an additional request, like the way [web bugs][18] usually transfer data. The dynamic baselining feature then finds out normal response times for the individual steps, so it can learn and alert on abnormal behavior in realtime, without requiring manual configuration of thresholds. 

根据AppDnamics公布的信息，他们的监控方式与其它厂商的主要区别是他们的动态基线技术，这项技术可收集浏览器指标和网络延迟，并增强了收集到数据传输回APM服务器的方式。运行于应用程序服务器上的代理程序插入一小段JavaScript代码来收集数据。这段程序收集数据并在下次请求中将数据发送回去，而不是采用像[web bugs][18]通常使用的，通过发起一次额外的请求传输数据的方式。动态基线功能可以找出正常的响应时间，因此它可以学习到正常的响应时间从而在异常行为发生时实时给出警告，而无需手工配置警告阈值。

   [18]: http://en.wikipedia.org/wiki/Web_bug

Additionally AppDynamics EUM provides basic analytic features, similar to what Google Analytics provides. They allow visualizing the number of calls and response times per browser or geographic region. 

此外，AppDynamics EUM提供了基本的、类似Google Analytics提供的分析功能。能够可视化的显示请求数量，及按每种浏览器或地理区域划分的响应时间。

The EUM feature is part of AppDynamics Pro and is available for SaaS customers right now. It is expected to be available for on-premise deployments with the release of version 3.4, currently scheduled for end of March. 

EUM功能是AppDynamics Pro的组成部分，SaaS客户现在已经可以使用。该功能预计在本地安装版（on-premise）版本3.4中可用，目前计划的发布时间是3月底。

  * **This article is part of a featured topic series on** [Java][19]
  * See more Java content at: [http://www.infoq.com/java][19]

   [19]: http://www.infoq.com/java

  * Other recent content items in this topic
  *     * [Book Review and Interview: Java Performance, by Charlie Hunt and Binu John][20]
    * [Oracle and the Java Ecosystem][21]

   [20]: http://www.infoq.com/articles/book-java-performance
   [21]: http://www.infoq.com/articles/oracle-java-ecosystem
   
**查看英文原文：**[AppDynamics Extends APM Solution to Include End User Monitoring][22]

[22]: http://www.infoq.com/news/2012/03/appdynamics-end-user-monitoring


