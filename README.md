# Paper Reading -- Deep Learning Infra

===

比做算法的懂工程落地，比做工程的懂算法模型。

1. deep learning: 算法、inference 部署、训练框架
2. 高性能计算
3. 芯片 & 硬件体系结构
4. c++ / python 语言
5. 存储与文件系统: deep learning 的重要 infra

## C++ & GPU 编程

### Reading List

- [A Tour of C++](01-zettelkasten/02-References/A%20Tour%20of%20C++.md)
- CUDA BY EXAMPLE: And Introduction to General-Pirpose GPU Programming
- CUDA Application Design and Development

## 高性能计算

### Reading List

- [深入理解计算机系统](01-zettelkasten/05-Notes%20Block/Computer%20Systems%20-%20A%20Programmer-s%20Perspective.md) 编译器级性能优化，存储器层次结构。进程通信。
- [计算机体系结构 - 量化研究方法](01-zettelkasten/02-References/Computer%20Architecture%20-%20A%20quantitative%20Approach.md) 并行优化的理论体系。存储的层级结构，指令级优化，SIMD 数据并行，线程级并行等。
- [计算机组成与设计 - 硬件/软件接口](01-zettelkasten/05-Notes%20Block/Computer%20Organization%20and%20Design%20-%20The%20Hardware%20and%20Software%20Interface.md) 指令级，CPU 流水线，存储器的层级结构

全都用大量篇幅讲存储器的层次结构。

TODO  补充 deep learning 的高性能计算

### Notes

- [HPC Learning Timline](01-zettelkasten/06-Content%20Maps/HPC%20Learning%20Timline.md) 我的 HPC 学习时间线
- [Learn Modern Cpp](01-zettelkasten/06-Content%20Maps/Learn%20Modern%20Cpp.md) 语言基础 -- Modern Cpp 学习地图
- [perf-tools-and-docs](01-zettelkasten/06-Content%20Maps/perf-tools-and-docs.md) 性能调优的工具 & 工具使用文档
- [Computer Hardware Introduction](01-zettelkasten/06-Content%20Maps/Computer%20Hardware%20Introduction.md) 计算机硬件科普
- [performance optimization](01-zettelkasten/06-Content%20Maps/performance%20optimization.md)  处理性能优化地图，以 CPU 为主

- [cgroups 详解](pdf/linux-kernel-and-perf/cgroups-intro.pdf)
- [Linux Performance Analysis and Tools](pdf/linux-kernel-and-perf/linux-performance-analysis-and-tools.pdf)
- [OpenMP tutorial](https://hpc.llnl.gov/tuts/openMP) one of the eight tutorials in the 4+ day "Using LLNL's Supercomputers" workshop
- [CUDA tutorial with code](cpp-notes/cuda-tutorial/README.md)

## 自动驾驶

### Tutorials

- [Apollo & Udacity 开放课程](https://apollo.auto/devcenter/devcenter_cn.html)
- [apollo3.5 Cyber架构讲解记录](https://zhuanlan.zhihu.com/p/56053077) 百度-王柏生
- [多伦多大学开放课程-自动驾驶汽车](https://www.coursera.org/specializations/self-driving-cars) 较为详细的分模块介绍, slides 和 scripts 质量很高
- :thumbsup: [Apollo 规划技术详解](https://bit.baidu.com/productsBuy?id=82) 主讲人是 百度 EM planner paper 的作者, 7 个视频, 1 倍速看完预计 4h
- [Robot Motion Planning](https://www.cs.cmu.edu/afs/cs/academic/class/15381-s07/www/slides/020807motion.pdf) pdf slide, 非常干货
- [Apollo轨迹规划技术分享](https://www.cnblogs.com/liuzubing/p/11051390.html)
- [解析百度Apollo之决策规划模块](https://paul.pub/apollo-planning/)
- [自动驾驶中的车辆运动学模型](https://zhuanlan.zhihu.com/p/103834150) 自行车模型(Bicycle Model), 阿克曼转向几何(Ackerman Turning Geometry)是一种为了解决交通工具转弯时，内外转向轮路径指向的圆心不同的几何学。
- [无人驾驶汽车系统入门（五）——运动学自行车模型和动力学自行车模型](https://blog.csdn.net/AdamShan/article/details/78696874) 运动学自行车模型的Python实现
- [Github: YannZyl/Apollo-Note](https://github.com/YannZyl/Apollo-Note) Note for Apollo 3.0 perception, prediction and planning modules

### 自动驾驶 Lectures

- [MIT 开放课程-Self-Driving Cars](https://selfdrivingcars.mit.edu/) Waymo 等公司的 lecture
- [Tesla Autonomy Day 2019](https://www.youtube.com/watch?v=-b041NXGPZ8&t=7371s)
- [Inside Nvidia's AI Infrastructure for Self-Driving Cars](https://www.youtube.com/watch?v=__eCwQxZFv8&t=226s)
- [Autonomous Driving by Cruise Lead](https://www.youtube.com/watch?v=s-8cYj_eh8E)

### Paper - Motion Planning 决策规划

- [Optimal and Efficient Path Planning for Partially-Known Environments](http://robotics.caltech.edu/~jwb/courses/ME132/handouts/Dstar_icra94.pdf) 1994, D* 算法

### Paper - Control 控制系统

- [A Learning-Based Tune-Free Control Framework for Large Scale Autonomous Driving System Deployment](https://arxiv.org/ftp/arxiv/papers/2011/2011.04250.pdf) Apollo 的自动调参控制框架
- [An Automated Learning-Based Procedure for Large-scale VehicleDynamics Modeling on Baidu Apollo Platform](https://www.researchgate.net/publication/338945678_An_Automated_Learning-Based_Procedure_for_Large-scale_Vehicle_Dynamics_Modeling_on_Baidu_Apollo_Platform) Apollo 的车辆动力学模拟, learning based model,
- [Toward a Comfortable Driving Experience for a Self-Driving Shuttle Bus](https://www.mdpi.com/2079-9292/8/9/943) 基于福田大客车研究 acc & jerk, 适用于 self-driving 和小汽车.

### 可视化

- [自动驾驶主流可视化工具对比（cruise/uber/Apollo/waymo）](https://zhuanlan.zhihu.com/p/113026573)
- [Uber和Cruise开源自动驾驶的可视化工具](https://zhuanlan.zhihu.com/p/57279694)
- [Cruise 开源了可视化平台Webviz，以提升自动驾驶研究水平](https://zhuanlan.zhihu.com/p/71190270)
- [AVS 3D Web 自动驾驶可视化+伯克利开源项目+Uber开源项目](https://zhuanlan.zhihu.com/p/152382225)
- [运行apollo3.5并体验dreamview可视化效果](https://zhuanlan.zhihu.com/p/56089471)

## Deep Learning 基础理论

- [[Paper Reading] 经典 CNN model -- 从 AlexNet 到 ResNet](topic-reviews/CNN-models--From-AlexNet-to-ResNet.md) 读三个经典实用模型的论文：AlexNet、VggNet、ResNet
- [[Paper Reading] Learning with Noisy Label -- 深度学习落地](topic-reviews/learning-with-noisy-labels.md) 当前研究热点，semi-supervised learning 流派越来越抢眼

## NLP

_Basic Models_

- Speech and Language Processing | [pdf](pdf/speech-and-language-processing-ed3.pdf)
- A Stochastic Parts Program and Noun Phrase Parser for Unrestricted Text | [pdf](pdf/a-stochastic-parts-program-and-noun-phrase-parser-for-unrestricted-text.pdf)
- A Statistical Approach to Machine Translation | [pdf](pdf/a-statistical-approach-to-machine-translation.pdf)
- Spam Filtering with Naive Bayes – Which Naive Bayes? | [pdf](pdf/spam-filtering-with-naive-bayes-which-naive-bayes.pdf)

_Undirected Graphical Model_

alias: Markov network, Markov Random Field (MRF)

HMM, MEMM, CRF

- introduction to Hidden Markov Model [pdf](pdf/speech-and-language-processing-ed3.pdf) Chap.8 Part-of-Speech Tagging
- Conditional Random Fields - Probabilistic Models for Segmenting and Labeling Sequence Data | [pdf](pdf/conditional-random-fields-probabilistic-models-for-segmenting-and-labeling-sequence-data.pdf)

_Near-duplicate Detection_

- N-gram Similarity and Distance | [pdf](pdf/n-gram-similarity-and-distance.pdf)
- A Closer Look at Skip-gram Modelling | [pdf](pdf/a-closer-look-at-skip-gram-modelling.pdf)
- Similarity Estimation Techniques from Rounding Algorithms | [pdf](pdf/charikar-estim.pdf)
- Detecting Near-Duplicates for Web Crawling | [pdf](pdf/simhash-detecting-near-duplicates-for-web-crawling.pdf)

## 搜索引擎

- Web search for a planet: The Google cluster architecture | [pdf](pdf/googlecluster-ieee.pdf)

## 图理论

- Finding and evaluating community structure in networks | [pdf](pdf/finding-and-evaluating-community-structure-in-networks.pdf)
- Fast algorithm for detecting community structure in networks | [pdf](pdf/fast-algorithm-for-detecting-community-structure-in-networks.pdf)

## 数据库系统

papers

- Bitcask - A Log-Structured Hash Table for Fast Key/Value Data | [pdf](pdf/bitcask-intro.pdf) | [notes](notes/bitcask-intro.md)
- The Google File System | [pdf](pdf/gfs-sosp2003.pdf) | [notes](notes/gfs-sosp2003.md)
- Bigtable: A Distributed Storage System for Structured Data | [pdf](pdf/bigtable-osdi06.pdf)
- The Chubby lock service for loosely-coupled distributed systems | [pdf](pdf/chubby-osdi06.pdf)

## 分布式系统

papers

- Brewer’s Conjecture and the Feasibility of Consistent, Available, Partition-Tolerant Web | [pdf](pdf/brewers-conjecture-sigact.pdf) | [notes](notes/brewers-conjecture-sigact.md)
- BASE: An Acid Alternative | [pdf](pdf/base-an-acid-alternative.pdf) | [notes](notes/base-an-acid-alternative.md)
- Eventually consistent | [pdf](pdf/eventually-consistent.pdf)
- Conflict-free Replicated Data Types | [pdf](pdf/conflict-free-replicated-data-types.pdf)
- The Byzantine Generals Problem | [pdf](pdf/lamport82.pdf)
- The Part-Time Parliament | [pdf](pdf/The-Part-Time-Parliament.pdf)
- Paxos Made Simple | [pdf](pdf/paxos-simple.pdf)
- MapReduce: Simplified Data Processing on Large Clusters | [pdf](pdf/mapreduce-simplified-data-processing-on-large-clusters.pdf) | [notes](notes/mapreduce-simplified-data-processing-on-large-clusters.md)
