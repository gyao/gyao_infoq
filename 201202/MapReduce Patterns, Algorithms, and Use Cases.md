MapReduce Patterns, Algorithms, and Use Cases
MapReduce模式、算法和用例
====

From: <http://www.infoq.com/news/2012/02/MapReducePatterns?>
  

With the explosion of Hadoop and big data usage, many people are currently looking for approaches to convert their existing implementations into MapReduce. Unfortunately, with the notable exception of ["Data-Intensive Text Processing with MapReduce"][10] and ["Mahout in Action"][11] there are very few publications dedicated to the designing of MapReduce implementations. In his new article, ["MapReduce Patterns, Algorithms, and Use Cases"][12] Ilya Katsov provides a systematic overview of problems that can be solved using a MapReduce framework. 

随着Hadoop和大数据应用的爆发式增长，很多人正在寻找将他们已有的实现转为MapReduce方式的方法。不幸的是，除了[《应用MapReduce进行数据密集的文本处理》][10]和[《Mahout in Action》][11]几本有名书籍之外，很少有关设计MapReduce实现的出版物。在新文章[“MapReduce模式、算法和用例”][12]中，Ilya Katsov提供了一个系统化的综述，阐述了能够应用MapReduce框架解决的问题。

   [10]: http://www.amazon.com/Data-Intensive-Processing-MapReduce-Synthesis-Technologies/dp/1608453421
   [11]: http://www.amazon.com/Mahout-Action-Sean-Owen/dp/1935182684/ref=sr_1_1?s=books&ie=UTF8&qid=1327246973&sr=1-1
   [12]: http://highlyscalable.wordpress.com/2012/02/01/mapreduce-patterns/

It starts with a fairly straightforward usage of MapReduce as a general purpose parallel execution framework, which can be applicable to many implementations requiring leveraging of large clusters for compute and data intensive calculations, including physical and engineering simulations, numerical analysis, performance testing, etc. The next group of algorithms, commonly used in Log Analysis, ETL and Data Querying, includes counting and summing, data collating (based on specific functions), filtering, parsing, validation and sorting. 

文章开始描述了一个非常简单的、作为通用的并行计算框架的MapReduce应用，这个框架适用于很多要求大量节点进行的计算和数据密集型计算，包括物理和工程仿真，数值分析，性能测试等等。接下来是一组算法，通常用于日志分析、ETL和数据查询，包括计数及求和，数据整理（基于特定函数），过滤，解析，验证和排序。

The second large group of MapReduce patterns, discussed by Katsov includes multiple relational MapReduce patterns, often used by data warehousing applications. These patterns are widely leveraged by Hive and Pig implementations and include predicate/function based data selection, data projection, data union, difference and intersection and groupBy aggregations. A separate discussion is dedicated to implementing data joins and include such algorithms as repartition joins and replicated joins 

第二大部分是关于MapReduce模式，Katsov讨论了包括多关系形MapReduce模式，通常用于数据仓库应用程序。这些模式在Hive和Pig实现中广泛使用，并包括基于推断/函数的数据选择，数据预测、数据联合、差分、交集和分组等聚集计算。另一个讨论是关于实现数据关联和包含等算法，例如reparition join和重复联合。

Moving further up the chain of complexity, the article discusses more complex MapReduce processing algorithms, including graph processing, search algorithms (breadth first search), page rank and data aggregation algorithms that can be leveraged in graph analysis, web indexing and general search applications. It also covers common text analysis and market analysis use cases requiring cross correlation calculation. This part covers both "pairs" and "stripes" design patterns and their comparative merits. 

更进一步，这篇文章讨论了更为复杂的MapReduce处理算法，包括图处理、搜索算法（广度优先搜索）、page rank数据集合算法，这些算法应用于图分析、web索引和通用搜索应用。文章也涵盖了常见的、需要互相关计算的文本分析和市场分析的用例。这部分包含了”pairs“和”stripes”设计模式和它们的相对优劣。

Finally, Katsov provides a good bibliography of more complex MapReduce implementations in the field of machine learning. 

最后，Katsov给出了一个在机器学习领域实现更复杂MapReduce的很好的参考书目。

Most of the algorithms, described in the article are accompanied by pseudo code and basic information for their applicability, advantages and disadvantages and some real world use cases. 

文中描述的大多数算法都有伪代码描述及它们的适用性，优势、劣势和一些真实的用例。

Many people today are still struggling with applicability of Hadoop and MapReduce for solving their business problems. Some still consider it a "technical approach in search of a business problem". The article is an important step in filling an existing void in the field of MapReduce algorithms, use cases and design patterns. It shows MapReduce’s power far beyond infamous "word count" and the ways it can be leveraged for solving a wide range of practical problems. 

如今很多人仍面临应用Hadoop和MapReduce解决业务问题的困扰。有些人仍然认为MapReduce是“搜索业务问题领域的技术手段”。这篇文章是填补MapReduce算法、用例和设计模式空缺的重要一步。它展示了MapReduce强大的力量，而不仅仅是用那个声名狼藉的“词语计数”例子，并显示了MapReduce可以解决众多实际问题的方式。

