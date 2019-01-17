# DesignPhilosophyDevelopPatternTree
设计哲学与开发模式

###架构哲学
https://blog.csdn.net/romandion/article/details/80177593


<pre>
          所谓哲学，即透过事务的表面现象，通过客观理性的分析，找出更接近事物本质的通用解。
      从而以一种大宇宙的视觉，来观察和解读这个世界的种种显现。
     
      1）大道至简
         软件爱你产品最终是给机器去执行的，但更重要的还是，要给别人去读懂的。没有一个复杂的
      系统是能给所有人读懂的，也没有人愿意去维护一个极度复杂的系统。
      2）高度模块化
         高内聚低耦合
         软件研发是要团队配合才能完成的作品，那么，团队的每个成员最终都只能分到系统中的一个
      小功能，那么怎样才能让每个人专心做好自己的工作，而不要停留在被别人打断和不断的打断别
      人这样的低效模式里面呢？答案就是高度模块化的设计，事先只需要由架构师约定模块之间的
      依赖，具体的实现交由各模块独立实现，外部不做接口约定之外的任何约束。
      3）可线性扩展
         有了OOP,有了继承，有了多态。
      5）需求变更是每天存在的
      6）面向对象思想对应的哲学思想就是世界是由物质组成的，物质之间是有联系的，物质是运动
         变化的。
      7）MVC设计模式对应的哲学思想就是分而治之，把大问题分解为小问题，把复杂问题分解为简单
         问题
      8）时间与空间的复杂度问题对应的哲学思想就是鱼与熊掌不可兼得，这世界不能追求完美，只能
         追求利益的平衡点
</pre>

<pre>
      
      1) 单一职责原则
         Single Responsibility Principle，简称是SRP.
         这个原则存在争议之处在哪里呢？就是对职责的定义，什么是类的职责，以及怎么划分类的职
         责。我们先举个例子来说明什么是单一职责原则

      2) 里氏替换原则
         在面向对象的语言中， 继承是必不可少的、非常优秀的语言机制，它有如下优点：
             1） 代码共享，减少创建类的工作量，每个子类都拥有父类的方法和属性；
             2） 提高代码的重用性；
             3） 子类可以形似父类，但又异于父类，”龙生龙，凤生凤，老鼠生来会打洞“是说子拥
                 有父的”种“，”世界上没有两片完全相同的叶子“是指明子与父的不同；
             5) 提高代码的可扩展性，实现父类的方法就可以”为所欲为“了，很多开源框架的扩展
                接口都是通过继承父类来完成的；
             6) 提高产品或项目的开放性。

         自然界的所有事物都是优点和缺点并存的，即使是鸡蛋，有时候也能跳出骨头来，继承的缺点如下：
             1) 继承是侵入性的。只要继承,就必须拥有父类的所有属性和方法；
             2) 降低代码的灵活性。子类必须拥有父类的属性和方法，让子类自由的世界中多了些约束；
             3) 增强了耦合性。当父类的常量、变量和方法被修改时，必需要考虑子类的修改，而且
                在缺乏规范的环境下，这种修改可能带来非常糟糕的结果——大片的代码需要重构。

      3) 依赖倒置原则
         1） 高层模块不应该依赖低层模块，两者都应该依赖其抽象；
         2） 抽象不应该依赖细节；
         3） 细节应该依赖抽象。

         采用依赖倒置原则可以减少类间的耦合性，提高系统的稳定性，减少并行开发引起的风险，
         提高代码的可读性和可维护性。

      5）接口隔离原则
         1）建立单一接口，不要建立臃肿庞大的接口，将接口尽量细化，同时接口中的方法应该尽量少。

         接口隔离原则与单一职责的定义的规则是不相同的，单一职责要求的是类和接口职责单一，
         注重的是职责，没有要求接口的方法减少

      6）迪米特法则
         一个对象应该对其他对象有最少的了解。通俗地讲，一个类应该对自己需要耦合或调用的类知
         道得最少，你（被耦合或调用的类）的内部是如何复杂都和我没关系，那是你的事情，我就知
         道你提供的这么多public方法，我就调用这么多，其他的我一概不关心。

      7）开闭原则
         一个软件产品只要在生命期内，都会发生变化，既然变化是一个既定的事实，我们就应该在设
         计时尽量适应这些变化，以提高项目的稳定性和灵活性，真正实现“拥抱变化”。开闭原则告诉
         我们应尽量通过扩展软件实体的行为来实现变化，而不是通过修改已有的代码来完成变化，它
         是为软件实体的未来事件而制定的对现行开发设计进行约束的一个原则
</pre>
