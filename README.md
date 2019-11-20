# An_Ontology_based_Hybrid_Approach_to_Course_Recommendation_in_Higher_Education

#### 介绍
博士论文：An_Ontology_based_Hybrid_Approach_to_Course_Recommendation_in_Higher_Education


## 章节-5 实验和结果

为了评估OPCR框架，使用Java编程语言实现了一个基于Web的原型系统。OPCR框架中的所有模块都是在后端使用开源工具实现的。原型系统被标记为OPRCourse，它是一个基于java的应用程序，具有web界面。利用protégé工具构建并验证了本体模型。实验中使用的数据都是从多个数据源中提取的实时信息。原型应用程序可通过位于oprscourse.ee.port.ac.uk的朴茨茅斯大学子域公开访问。在分析完成之前，该网站一直处于活动状态。为了实现课程领域和作业领域的数据集成，实现了基于web爬虫的本体。爬网程序可以在许多不同的域中使用，并对后端代码进行某些更改，以便与域的要求相匹配。所有代码都可以在github.com的author帐户上通过以下链接供开发人员和研究人员使用：

https://github.com/mohammediraq/OPCR

本章介绍了原型系统的实现，首先介绍了原型系统的全部操作功能，从UCAS等教育机构收集的数据开始，接着进行本体模型的构建和本体映射，最后给出评分和建议。
原型应用程序是在Windows 7下的Intel（R）Core（TM）2dup处理器上实现和运行的，该处理器的CPU为3.20ghz，内存为16gb。HTML用于系统接口，MySQL服务器用于分配系统数据集和用户评级。protégé工具还用于评估系统中构建的本体


### 5.1 Data Source and Configuration

在该系统中，用于实现OPCRa的所有数据都来自免费的开源资源。课程信息是从UCAS.com网站提取的，工作信息是从reast.com网站提取的。NNS分数信息来自officeforstudents.org.uk网站，大学排名信息来自guardain.com。然而，这些信息大多是非结构化的。为了组织这项工作，我们设计并定制了一个网络爬虫程序。利用收集到的数据，基于获取的知识，构建项目本体（课程和作业）。没有现有的特定数据集，可以应用于设计模型中实现。因此，创建了一个名为ontologyset的数据集，其中包括从UCAS.com提取的课程。然而，不需要建立一个基准数据集来评估OPCR的性能。系统元数据包括ontologyset的近21000个在线课程，涵盖了从UCAS.com存档的70个不同主题领域。这些都是从联合王国各大学和学院的不同部门选择和下载的，用于测试目的。细目是从这些学科领域中挑选出20门课程，但决定使用计算机科学和商业管理课程。课程科目按高等教育科目分类法（HECoS）进行分类。请参阅附录A和表A.1和表A.2，表A.1和表A.2显示了信息技术、商业和管理领域的科目分类。数据集中的课程涵盖所有研究生学术水平，产生了一套具有代表性的课程，其中包括在不同大学提供的各种课程。对于工作信息，确实网站被用作提取工作信息的来源。此信息包括职务、说明、薪资、位置和用户评论。出于测试目的，提取了与CS和BAM课程相关的任何作业。

#### 5.1.1 Data Collection Module 

Web服务器环境对它们集成的软件提出了特殊的要求。典型的Java web应用服务器（比如Tomcat）在单独的线程中处理每个HTTP请求。当请求进入时，请求处理程序将被激活；如果它需要数据库访问，它将打开一个连接（通常来自连接池），执行所需的处理并将数据库连接返回到该池。有些体系结构甚至在更短的时间内将数据库连接租给请求处理程序，例如每个数据库操作一次。

#### 5.1.2 Web Crawler 

爬虫程序是使用Java框架（JDK1.8版）和NetBeans（8.02版）开发的，NetBeans作为Windows平台上的开发工具，如附录C所示。该系统在任何标准机器上运行，不需要任何特定硬件才能有效运行。从UCAS下载了大约6000个网页，并将它们的链接记录在数据库中。这项实验的重点是“计算机科学课程”中的一个爬行主题。参考本体模型是使用protégé工具创建的。使用基于web的用户界面来提示用户给出查询，如图5.1所示。





5.2 Application of OPCR
5.2.1 5.2.2
5.2.2.1
OPCR Interface ............................................................................................................. 87 Ontology model............................................................................................................. 91 Ontology Construction Module ................................................................................ 92 5.2.2.2 Ontology Mapping Implementation.............................................................................. 94 5.2.3 Recommendation Producing ......................................................................................... 96 5.2.3.1 Content Based Filtering .



