# Code Visualization
## [What]什么是代码可视化？
> Code visualization is the process of creating graphical representations of source code to help understand and analyze it.  
代码可视化是创建源代码的图形表示以帮助理解和分析它的过程。

**个人理解**：通过使用图形化手段（架构图、依赖图、分布式追踪、类图、火焰图、CallGraph等）使代码在某些特征上变得可观测，用于辅助开发人员理解分析项目或建设一些自动化工具。

## [Why]为什么需要代码可视化?
下面通过几个场景来说明开发、测试同学为什么需要代码可视化功能：

### 场景1：代码逻辑理解困难
项目代码量很大且需求迭代快，每次梳理的文档很快就过时了。新同学入手困难苦不堪言，老手也很难对项目整体的业务逻辑有一个全面的认知，常常需要重新梳理逻辑。  
<img src="imgs/readme-picture-1.png" width="1000" height="400" alt="代码逻辑理解困难">

### 场景2：代码改动影响面难以评估
需求的诉求是修改A页面的逻辑，但由于后端代码很多公用逻辑且调用层级很深，上线才后发现影响了B页面的逻辑，造成了线上事故。  
<img src="imgs/readme-picture-2.png" width="1000" height="400" alt="影响面难以评估">

### 场景3：遗留项目重构缺少抓手
老旧遗留项目经过长时间迭代和多次更换团队，导致内部代码逻辑十分混乱且没人能完全讲明白所有逻辑。但新的业务迭代需求源源不断，在原有项目上修改成本越来越高，亟需重构以获得更高地研发效率。  
<img src="imgs/readme-picture-3.png" width="500" height="400" alt="遗留项目重构">

**其他场景**：代码改动影响面评估不准导致自动化case编写困难，回归也常常覆盖不到关联逻辑；线上问题排查困难，难以快速定位到出错代码......

## [How]怎么实现代码可视化?
大体可以分两步走：
- 第一步**程序分析**：获取到源码、各种中间表示方式或其他方式采集的数据形成可视化的数据基础；
- 第二步**数据可视化**：根据想要观测的视角选择对应的图表类型，将第一步获取的数据进行可视化展示。  

当然对于实际应用场景完成可视化也只是刚刚开始，之后会再基于可观测的部分结合自己的诉求建设更复杂的工具。本书将会从理论和实践两部分进行阐述，先了解实现代码可视化需要掌握的基础理论，例如：AST生成、CFG和DFG等；接着实践部分我们会实现“**CallGraph可视化**”并提供基于Git的代码影响变更分析功能；最后会罗列一些业界已知的实践方案供大家扩展学习。  
信息结构参考下面的思维导图（图内容还在迭代中，原图获取[点这里](base/code-visualization-map.xmind)）:
![代码可视化导图](imgs/readme-picture-4.png)

---
### 本书适合谁
- 喜欢研究源码且深知源码本身蕴藏信息拥有无限可能
- 对编译原理、程序分析感兴趣
- 想要解决实际业务中因代码理解不足而导致的各种问题
- 喜欢将一切事物可视化，视觉系才是最diao的
- 仅仅是想多学一点，或掌握一门装*技术  
......

### 本书内容概览
（更新中......）
* [前言](README.md)
* [原理篇](base/Principle.md)
    * [编译器](base/Compiler.md)
        * [编译器前端](base/Compiler-Front.md)
        * [编译器中端](base/Compiler-Mid.md)
    * [程序分析](base/Program-Analysis.md)
    * [可视化图类型](base/Graph.md)
* [实践篇](practice/Practice.md)
    * [手搓工具](practice/Tools.md)
        * [生成CallGraph](TBD)
        * [代码影响变更分析](TBD)
    * [业界实践](TBD)
        * [ArchGuard](TBD)
        * [代码阅读工具](TBD)
        * [代码理解技术](TBD)
        * [精准测试](TBD)
        * [风险识别](TBD)
        * [代码缺陷识别](TBD)
* [结语](TBD)

### 交流联系
- Email: [xiexiao064@gmail.com](mailto:xiexiao064@gmail.com)
- WeChat: ShawnLFF