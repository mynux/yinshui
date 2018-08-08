---
title: 任何好的code都是不断修改完善的过程
layout: post
tags: []
date: 2014-12-03 07:35:00.362000
---
以前以为好的code就像李白的斗酒诗百篇，王羲之的醉酒兰亭序，是一挥而就的产物。但读完此书的大部分篇章才发现，文章给人最大的感触就是所有的好的code都是经过不断的refactor，不但的修改，一步步的达到最终的效果。记得一位同事说过，其实我们开发的过程，大概只有四分之一的时间是用来完善设计文档中的功能，然后四分之三的时间都是用来不断的修改，重构直到完成我们最终的状态。 
　　这本书更像是一本programmer的枕边书，点很细，很实用。尤其在提高整体的代码质量上具有非常显著的效果。值得不但的品读，而且完全是目录就可以作为一个一个的tips来指导高质量的程序开发。 
　　比如在对于函数的说明上：    
    1. Small.  
    2. Do one thing  
    3. One level of Abstract per function   
    4. Replace some switch construct statement with abstract factory method.   
    5. Function parameters( Common one or two).   
    6. Have no side effect.   
    7. Prefer exception for return error code(error code is an old-fashion way!)   
    8. Don't re-invent the wheel!!! most refactor process lie in.   

值得说明的是，书的粒度比较细，虽然有很多Design层面的东西，但也往往是为了说明一些更细节的问题。有时也会发现书中的很多principle显的太多，太难以掌握，但其实随着经验的增长，代码量的增加，渐渐会发现有很多原则本质上是相同的，就比如repeat这个原则，当我们真正的做到，do one things and keep the function small, 很多时候也就能降低代码重复率了。再者对于one level of abstract per function 和抽象工厂模式，很多时候在一些代码中如果我们不用抽象工厂模式就会在程序逻辑中引入了对象构造本身的工作，而这另一方面就会导致程序逻辑中显的混乱，比如不再是do one thing, 或者不再是on the level abstract level.   

再者，比如书中提到了AOP经典模式的应用，log4j, transaction process等都可以通过如俄罗斯套娃般的proxy reflection来解决。然和深入的分析了proxy的实现方法，这些都给人一种焕然一新的感觉。

---From Robert C. Martin Clean Code  
[豆瓣原文](http://book.douban.com/review/7218998/)
