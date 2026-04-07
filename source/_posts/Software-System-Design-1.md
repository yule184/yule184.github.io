---
title: 软件系统设计-设计模式部分-part 1
date: 2026-04-03 18:45:43
tags:
    - 学习
    - 软件系统设计
categories:
    - 大三 
---

九乡河文理学院/苏州校区/NULL学院/乙巳年-丙午年春学期/软件系统设计课程笔记

设计模式部分，LYF老师授课，主要内容是一些设计模式

<!-- more -->

# 0-概述
## 软件模式
软件模式是将模式的一般概念应用于软件开发领域，即**软件开发的总体指导思路或参照样板**。软件模式并非仅限于设计模式，还包括架构模式、分析模式和过程模式等，实际上，**在软件生存期的每一个阶段都存在着一些被认同的模式**。

软件模式可以认为是对软件开发这一特定“问题”的“解法”的某种统一标识，软件模式等于一定条件下的出现的问题以及解法。软件模式的基础结构由4个部分构成：

{% quote blue %}
+ 问题描述
+ 前提条件（环境或约束条件）
+ 解法
+ 效果

{% endquote %}

<!-- 这是一张图片，ocr 内容为： -->
![22.png](https://picui.ogmua.cn/s1/2026/04/03/69cf9d8b387ca.webp)

软件模式与具体的应用领域无关，在模式发现过程中需要遵循**大三律（Rule of Three）**，只有经过**三个以上不同类型（或不同领域）的系统**的校验，一个解决方案才能从候选模式升格为模式。

## 设计模式
### 定义
设计模式（Design Pattern）是**一套被反复使用、多数人知晓的、经过分类编目的、代码设计经验的总结**，使用设计模式是为了可重用代码、让代码更容易被他人理解、保证代码可靠性。

### 基本要素
设计模式一般有如下几个基本要素：模式名称、问题、目的、解决方案、效果、示例代码和相关设计模式，其中的关键元素包括以下四个方面：

{% quote blue %}
+ 模式名称 Pattern Name
+ 问题 Problem
+ 解决方案 Solution
+ 效果 Consequences
{% endquote %}


<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/54587098/1775098652868-9bde8e4c-ac6d-4ef9-bc20-84bbc120c5fd.png)

### 分类
根据其<u>目的</u>（模式是用来做什么的）可分为 **创建型（Creational）、结构型（Structural）和行为型（Behavioral）** 三种：

+ 创建型模式主要用于**创建对象**
+ 结构形模式主要用于**处理类或对象的组合**
+ 行为型模式主要用于**描述对类或对象怎样交互和怎样分配职责**

根据<u>范围</u>，即模式主要是用于处理类之间关系还是处理对象之间关系，可分为类模式和对象模式两种：

+ <font style="color:rgba(0, 0, 0, 0.75);">类模式</font>**<font style="color:rgba(0, 0, 0, 0.75);">处理类和子类之间的关系</font>**<font style="color:rgba(0, 0, 0, 0.75);">，这些关系通过继承建立，在编译时刻就被确定下来，是属于</font>**<font style="color:rgba(0, 0, 0, 0.75);">静态</font>**<font style="color:rgba(0, 0, 0, 0.75);">的</font>
+ <font style="color:rgba(0, 0, 0, 0.75);">对象模式</font>**<font style="color:rgba(0, 0, 0, 0.75);">处理对象之间的关系</font>**<font style="color:rgba(0, 0, 0, 0.75);">，这些关系在运行时刻变化，更具</font>**<font style="color:rgba(0, 0, 0, 0.75);">动态</font>**<font style="color:rgba(0, 0, 0, 0.75);">性</font>

| **<font style="color:rgb(79, 79, 79);">范围/目的</font>** | **<font style="color:rgb(79, 79, 79);">创建型模式</font>** | **<font style="color:rgb(79, 79, 79);">结构型模式</font>** | **<font style="color:rgb(79, 79, 79);">行为型模式</font>** |
| :---: | :---: | :---: | :---: |
| **<font style="color:rgb(79, 79, 79);">类模式</font>** | <font style="color:rgb(79, 79, 79);">工厂方法模式</font> | <font style="color:rgb(79, 79, 79);">（类）适配器模式</font> | <font style="color:rgb(79, 79, 79);">模板方法模式</font> |
| **<font style="color:rgb(79, 79, 79);">对象模式</font>** | <font style="color:rgb(79, 79, 79);">抽象工厂模式   </font><font style="color:rgb(79, 79, 79);">建造者模式   </font><font style="color:rgb(79, 79, 79);">原型模式   </font><font style="color:rgb(79, 79, 79);">单例模式</font> | <font style="color:rgb(79, 79, 79);">（对象）适配器模式   </font><font style="color:rgb(79, 79, 79);">桥接模式   </font><font style="color:rgb(79, 79, 79);">组合模式   </font><font style="color:rgb(79, 79, 79);">装饰模式   </font><font style="color:rgb(79, 79, 79);">外观模式   </font><font style="color:rgb(79, 79, 79);">享元模式   </font><font style="color:rgb(79, 79, 79);">代理模式</font> | <font style="color:rgb(79, 79, 79);">命令模式   </font><font style="color:rgb(79, 79, 79);">迭代器模式   </font><font style="color:rgb(79, 79, 79);">中介者模式   </font><font style="color:rgb(79, 79, 79);">观察者模式   </font><font style="color:rgb(79, 79, 79);">状态模式   </font><font style="color:rgb(79, 79, 79);">策略模式</font> |




# 1-面向对象软件设计

将实现的约束条件应用到面向对象分析（OOA）所产生的概念模型的过程。

+ 用方法和属性来描述用于构成系统的类
+ 添加不明显属于领域的类，比如抽象类和接口
+ 描述类是如何构成组件的

OOA--OOD--OOP

## 如何发现合适的对象

{% quote blue %}
并非那个对象！
{% endquote %}

难点：将一个系统分解成对象

许多对象直接来自于分析模型或从实现空间（数据库、文件、用户界面、IPC）

使用策略模式（如果一个算法很可能会改变）：添加类来实现策略模式

从OOA到OOD没有循序渐进的简单方法，至少OOA以相当直接的方式给出了问题域组件。对于其他的部分，则需要经验

## 面向对象设计原则概述
软件的**可维护性（Maintainability）和复用性**

+ 较低的原因
    - 过于僵硬 _Rigidity_
    - 过于脆弱 _Fragility_
    - 复用率低 _Immobility_
    - 黏度过高 _Viscosity_
+ 好的性质
    - 可扩展性 _Extensibility_
    - 灵活性 _Flexibility_
    - 可插入性 _Pluggability_

**软件的复用(Reuse)或重用**拥有众多优点，如可以提高软件的开发效率，提高软件质量，节约开发成本，恰当的复用还可以改善系统的可维护性。

面向对象设计复用的目标在于**实现支持可维护性的复用**。

在面向对象的设计里面，**可维护性复用都是以面向对象设计原则为基础的**，这些设计原则首先都是复用的原则，遵循这些设计原则可以有效地提高系统的复用性，同时提高系统的可维护性。

面向对象设计原则也是对系统进行合理**重构**的指南针，**重构 (Refactoring)** 是在不改变软件现有功能的基础上，通过调整程序代码改善软件的质量、性能，使其程序的设计模式和架构更趋合理，提高软件的扩展性和维护性。

### 单一职责原则 Single Responsibility Principle/SRP
表述一：一个对象应该只包含单一的职责，并且该职责被完整地封装在一个类中

> Every object should have a single responsibility, and that responsibility should be entirely encapsulated by the class
>

表述二： 就一个类而言，应该仅有一个引起它变化的原因

> There should never be more than one reason for a class to change.
>

一个类（模块/方法）**承担的职责越多， 它被复用的可能性越小**。如果一个类承担的职责过多，就相当于将这些职责耦合在一起，当其中一个职责变化时，可能会影响其他职责的运作。

**类的职责**主要包括两个方面：**数据职责**和**行为职责**，数据职责通过其属性来体现，而行为职责通过其方法来体现。

单一职责原则是实现**高内聚、低耦合**的指导方针

### 开闭原则 Open-Closed Principle/OCP
一个软件实体应当对扩展开放，对修改关闭。也就是说在设计一个模块的时候，应当使这个模块可以在不被修改的前提下被扩展，即实现在不修改源代码的情况下改变这个模块的行为

> Software entities should be open for extension, but closed for modification
>

在开闭原则的定义中，软件实体可以指一个软件模块、一个由多个类组成的局部结构或一个独立的类。

+ 抽象化是开闭原则的关键
+ 对可变性封装原则 _Principle of Encapsulation of Variation/EVP_：要求找到系统的可变因素并将其封装起来

### 里氏代换原则  Liskov Substitution Principle/LSP
定义一： 如果对每一个类型为S的对象o1，都有类型为T的对象o2，使得以T定义的所有程序P在所有的对象o2都代换成o1时，程序P的行为没有变化，那么类型S是类型T的子类型。

> If for each object o1 of type S there is an object o2 of type T such that for all programs P defined in terms of T, the behavior of P is unchanged when o1 is substituted for o2 then S is a subtype of T.
>

定义二：所有引用基类（父类）的地方必须能透明地使用其子类的对象

> Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it.
>

通俗表述为：**在软件中如果能够使用基类对象，那么一定能够使用其子类对象**。

+ 把基类都替换成它的子类，程序将不会产生任何错误和异常
+ 反过来则不成立，如果一个软件实体使用的是一个子类的话，那么它不一定能够使用基类。

在程序中尽量使用基类类型来对对象进行定义，而在运行时再确定其子类类型，用子类对象来替换父类对象。

### 依赖倒转原则  Dependence Inversion Principle/DIP
高层模块不应该依赖低层模块，它们都应该依赖抽象。抽象不应该依赖于细节，细节应该依赖于抽象。

> High level modules should not depend upon low level modules, both should depend upon abstractions. Abstractions should not depend upon details, details should depend upon abstractions.
>

另一种表述：要针对接口编程，不要针对实现编程

> Program to an interface, not an implementation
>

代码要**依赖于抽象的类**，而不要依赖于具体的类；要**针对接口或抽象类编程**，而不是针对具体类编程。

+  如果说开闭原则是面向对象设计的目标的话，那么依赖倒转原则就是面向对象设计的主要手段

实现：在代码中使用抽象类，而将具体类放在配置文件中

类之间的耦合：

+ 零耦合关系
+ 具体耦合关系
+ **抽象耦合关系**

依赖倒转原则要求客户端依赖于**抽象耦合**，**以抽象方式耦合**是依赖倒转原则的关键



### 接口隔离原则  Interface Segregation Principle/ISP
客户端不应该依赖那些它不需要的接口。（接口指的是所定义的方法）

> Clients should not be forced to depend upon interfaces that they do not use.
>

另一种定义： 一旦一个接口太大，则需要将它分割成一些更细小的接口，使用该接口的客户端仅需知道与之相关的方法即可。

> Once an interface has gotten too 'fat' it needs to be split into smaller and more specific interfaces so that any clients of the interface will only know about the methods that pertain to them.
>

接口隔离原则是指使用**多个专门的接口**，而**不使用单一的总接口**。每一个接口应该承担一种相对独立的角色，不多不少，不干不该干的事，该干的事都要干

+ 一个接口就只代表一个角色，每个角色都有它特定的一个接口，此时这个原则可以叫做“角色隔离原则”
+ 接口仅仅提供客户端需要的行为，即所需的方法，客户端不需要的行为则隐藏起来，应当为客户端提供尽可能小的单独的接口，而不要提供大的总接口

使用接口隔离原则拆分接口时，首先必须满足**单一职责原则**，将一组相关的操作定义在一个接口中，且在满足高内聚的前提下，接口中的方法越少越好。

可以在进行系统设计时采用**定制服务**的方式，**为不同的客户端提供宽窄不同的接口**，只提供用户需要的行为，而隐藏用户不需要的行为。

### 合成复用原则 Composite Reuse Principle/CRP
> 又称组合/聚合复用原则
>

尽量使用对象组合，而不是继承来达到复用的目的

> Favor composition of objects over inheritance as a reuse mechanism
>

在一个新的对象里通过**关联关系**（包括**组合**关系和**聚合**关系）来使用一些已有的对象，使之成为新对象的一部分；新对象**通过委派调用已有对象的方法达到复用其已有功能的目的**

+ 尽量使用组合/聚合关系，少用继承
+  在面向对象设计中，可以通过两种基本方法在不同的环境中复用已有的设计和实现，即通过组合/聚合关系或通过继承。

**组合/聚合**可以使系统更加灵活，类与类之间的**耦合度降低**，一个类的变化对其他类造成的影响相对较少，因此一般首选使用组合/聚合来实现复用 ；

### 最小知识则/迪米特原则 Least Knowledge Principle, LKP/  Law of Demeter, LoD

1. 不要和陌生人说话 _Don't talk to strangers_
2. 只和你的直接朋友通信 _Talk only to your immediate friends_
3. 每一个软件单位对其他的单位都只有最少的知识，而且局限于那些与本单位密切相关的软件单位。   
_Each unit should have only limited knowledge about other units: only units "closely" related to the current unit._

简单地说，迪米特法则就是指**一个软件实体应当尽可能少的与其他实体发生相互作用**。

在迪米特法则中，对于一个对象，其朋友包括以下几类：
1. 当前对象本身(this)
2. 以参数形式传入到当前对象方法中的对象
3. 当前对象的成员对象
4. 如果当前对象的成员对象是一个集合，那么集合中的元素也都是朋友
5. 当前对象所创建的对象

任何一个对象，如果满足上面的条件之一，就是当前对象的“朋友”，否则就是“陌生人”。<br> 
在<u>狭义</u>的迪米特法则中，如果两个类之间不必彼此直接通信，那么这两个类就不应当发生直接的相互作用，如果其中的一个类需要调用另一个类的某一个方法的话，可以<u>通过第三者转发这个调用</u>。  

{% quote blue %}
可以降低类之间的耦合，但是会在系统中增加大量的小方法并散落在系统的各个角落，它可以使一个系统的局部设计简化，因为每一个局部都不会和远距离的对象有直接的关联，但是也会造成系统的不同模块之间的通信效率降低，使得系统的不同模块之间不容易协调。
{% endquote %}

<u>广义</u>的迪米特法则：指对对象之间的信息流量、流向以及信息的影响的控制，主要是对信息隐藏的控制

主要用途：**控制信息的过载**

+ 在类的划分上，应当尽量**创建松耦合的类**，类之间的耦合度越低，越有利于复用
+ 在类的结构设计上，每一个类都应当**尽量降低其成员变量和成员函数的访问权限**
+ 在类的设计上，只要有可能，**一个类型应当设计成不变类**
+ 在对其他类的引用上，**一个对象对其他对象的引用应当降到最低**。


# 2-策略模式
## 策略模式引入：鸭子

从SimUDuck应用程序开始

我们需要添加功能使得鸭子会飞，如果简单地修改鸭子父类（直接添加fly()）会导致橡皮鸭也会飞——不是所有的鸭子都会飞
- 考虑继承 
  - 我们总是可以像使用quack()方法一样在橡皮鸭中覆盖fly()方法… 
  - 但是，当我们在程序中添加木制诱饵鸭子时会发生什么呢？他们不应该飞或嘎嘎… 
  - 高管们希望每六个月更新一次产品。每次更新中都会有新的Duck子类，真是一场噩梦！ 
- 使用接口：导致代码无法复用 
  - 更改非飞行子类(继承，覆盖)VS 更改飞行子类(接口)

  
## 变更 Change

1. 软件开发过程中的一个常数  _The one constant in software development_
2. 很多事情都可以推动变化。列出一些您必须在应用程序中更改代码的原因 
   1. 在软件开发中编写一些更改 
   2. 我的客户或用户决定他们想要其他东西，或者他们想要新功能 
   3. 我的公司决定与另一家数据库供应商合作，并且还从另一家使用不同数据格式的供应商那里购买数据 
   4. 技术不断变化，我们必须更新代码以使用协议
3. 我们已经学到了足够的知识来构建我们的系统，我们想回去做点更好的事情
   

## 设计原理：封装各种变化

1. 对应实现的原则：**开闭原则**
2. 识别应用程序中各个方面，将其与保持不变的方面分开
3. 将变化的部分封装起来，以便以后可以更改或扩展变化的部分而不会影响那些不变的部分

### 将变化和保持不变分开  Separating what changes from what stays the same  

fly()和quack()是Duck类的一部分，它们在鸭子直接有所不同，为了将这些行为和Duck类分开，我们把这两种方法都从Duck类中拉出来，创建一组新的类来表示每种方法
   
### 设计鸭子行为  Designing the Duck Behaviors  
   
我们希望保持灵活性，将行为分配给鸭子的实例，可以动态地修改鸭子的行为（运行时）
   

## 设计原则：面向接口编程而不是面向实现

{% quote blue %}
对应实现的原则：依赖倒转原则

Program to an interface, not an implementation.  
{% endquote %}


### 表示行为的类

1. 不会由Duck类来实现flying和quacking的接口
2. 我们将制作一组类，**其全部目的是代表一种行为**。 
   1. 第一个解决方案：超类中的具体实现 
   2. 第二个解决方案：在子类本身中提供专门的实现**它们都依赖于实现**
      

### 回忆多态性(polymorphism)

1. “面向接口编程"实际上意味着"**面向超类型编程**”
2. 这里有接口的概念，但也有Java结构接口 
3. 你可以对接口进行编程，而不必实际使用Java接口
2. 变量的声明类型应该是超类型，通常是接口的抽象类，以便分配给这些变量的对象可以是超类型的任何具体实现，这意味着声明它们的类不必知道实际的对象类型！
3. 我们将行为抽象出来，同时分别具体了两个子类(实现了依赖倒转)，并且是完整的封装
   
### 在这个设计过程中
   
其他类型的对象可以重用我们的fly和quack行为，因为这些行为不再隐藏在我们的Duck类中。我们可以添加新行为，而无需修改任何现有行为类或触摸任何使用飞行行为的Duck类，这样，我们就可以在没有继承带来的所有负担的情况下获得复用的好处

{% quote blue %}
问：类只是一种行为，这感觉有点奇怪。类不应该代表事物吗？类不应该同时具有状态和行为吗？
   
答：在OO系统中，是的，类表示通常具有状态(实例变量)和方法的事物。在这种情况下，事情恰好是一种行为。但是，即使一个行为仍然可以具有状态和方法。飞行行为可能具有实例变量，这些变量代表飞行属性(每分钟的飞行节拍，最大高度和速度等)
{% endquote %} 

## 整合鸭子行为
   
关键在于，Duck现在将**委托**其飞行和鸣叫行为，而不是使用Duck类(或子类)中定义的quacking和flying方法
——**委托是调用另一个部分的方法**
   
> a Duck will now delegate its flying and quacking behavior, instead of using quacking and flying methods defined in the Duck class (or subclass)
> 

1. 首先将两个示例变量添加到Duck类中
2. 实现performQuack()
3. 设置飞行行为和叫行为实例变量
   

## 鸭子测试代码 Testing the code

1. 动态设置行为 Setting behavior dynamically
2. 制作新的鸭子类型 Make a new Duck type
3. 制作新的FlyBehavior类型 Make a new FlyBehavior type
4. 使ModelDuck具有火箭功能 Make the ModelDuck rocket-enabled


## HAS-A可以比IS-A更好
   
优先考虑组成而不是继承
   
合成为您提供了更多的灵活性，它不仅使您可以将一系列算法封装到自己的类集中，而且还使您可以在运行时更改行为
   

# 第一个设计模式-策略模式
   
**策略模式**定义了一系列算法，将每个算法封装在一起，并使它们可替换，策略使算法独立于使用该算法的客户端而变化
1. 变化在客户使用时才会出现，也就是要实现这个模式就必须要将细节暴露给用户。
2. 实际开发的时候，可能是由多个设计模式组合成的
3. 我们可能需要一个算法族，希望彼此是可以替换的
   
## 模式描述
   
名称：**策略模式 Strategy Pattern**
   
目的：定义一系列算法，封装每个算法，并使它们可替换。策略使算法可以独立于使用该算法的客户端而变化。
   
别名：Policy Pattern
   

## 模式动机——将文本流分成几行
   
存在许多用于将文本流分成行的算法。将所有这样的算法硬连接到类中是不可取的。
   
不满足开闭原则，每次修改都要反复检查每一个条件语句

````java
public class Context{
   public void algorithm(String type){
       if(type.equals("strategyA")) {
           this.strategy = new ConcreteStrategyA();
       }
       else if(type.equals("strategyB")) {
           this.strategy = new ConcreteStrategyB();
       }
       else if(type.equals("strategyC")) {
           this.strategy = new ConcreteStrategyC();
       }
   }
}
````

   
## 应用场景
   
在以下情况下使用策略模式

1. 许多相关的类仅在**行为**上有所不同，策略提供了一种使用多种行为之一配置类的方法
2. 您需要**算法的不同变体**。例如，您可能定义了反映**不同空间/时间权衡**的算法。将这些变体实现为算法的类层次结构时，可以使用策略。
3. 一种算法使用客户端不应该知道的数据。使用策略模式**可避免暴露复杂的、特定于算法的数据结构**
4. 一个类定义了许多行为，这些行为在其操作中显示为多个条件语句。代替许多条件，将相关的条件分支移到他们自己的**策略类**中。
   很多问题都出现于数据结构被暴露：比如**迭代器模式**。
   
## 模式使用的结果
1. 相关算法家族。策略类的层次结构定义了一系列算法或行为，以供上下文重用。继承可以帮助排除算法的通用功能。
2. 子类化的替代方法。
3. 策略消除条件语句。
4. 多种实现方式。策略可以提供相同行为的不同实现。客户可以选择具有不同时间和空间权衡的策略。
5. 客户必须意识到不同的策略。这种模式有一个潜在的缺点，即**客户在选择合适的策略之前必须先了解策略的不同**，不然客户可能会遇到实现问题。
6. 策略和上下文之间的通信开销 变大。
7. 对象数量增加。
8. 模式一般都会有的缺点：
   a. 增加设计的复杂度和增加类的个数(增加辅助类)
   b. 增加隔阂、方法调用，降低软件运行的效率，但是已经不是目前主要的问题了
9. **Java的加密方法、时间显示算**法等都是通过策略模式实现的

## 设计工具箱的工具
1. 面向对象的基础 OO Basics 
   1. 抽象 _Abstraction_ 
   2. 封装 _Encapsulation_ 
   3. 多态性 _Polymorphism_ 
   4. 继承 _Inheritance_
2. 面向对象原则 OO Principles
   1. 封装可变性 _Encapsulate what varies_
   2. 选择组合而不是继承 _Favor composition over inheritance_
   3. 面向接口编程，而不是面向实现编程 _Program to interfaces, not implementation_
3. 面向对象模式 OO Patterns：
   4. 策略 Strategy 
   5. 回顾 Reviews
1. 仅仅知道面向对象基础不能让你成一个很好的面向对象的设计人。_Knowing the OO basics does not make you a good OO designer._
2. 好的面向对象设计应该可以重用、扩展和稳定的 _Good OO designs are reusable, extensible and maintainable._
3. 模式让你知道如何创建一个有很好的面向对象设计质量的系统 _Patterns show you how to build systems with good OO design qualities_.
4. 模式是公认的面向对象的经验。_Patterns are proven object oriented experience._
5. 模式不会为您提供代码，它们会为您提供设计问题的一般解决方案。 您将它们应用于您的特定应用程序。_Patterns don’t give you code, they give you general solutions to design problems. You apply them to your specific application._
6. 模式不是发明的，而是被发现的。_Patterns aren’t invented, they are discovered._
7. 大多数模式和原则都解决软件变更问题。_Most patterns and principles address issues of change in software._
8. 大多数模式都允许系统的某些部分独立于所有其他部分而变化。_Most patterns allow some part of a system to vary independently of all other parts._
9. 我们经常尝试采用系统中的变化并将其封装。_We often try to take what varies in a system and encapsulate it._
10. 模式提供了一种共享语言，可以使您与其他开发人员的交流价值最大化。_Patterns provide a shared language that can maximize the value of your communication with other developer._


