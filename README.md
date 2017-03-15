# iOS中的设计模式总结

## 策略模式

概念

	定义一系列的算法,把它们一个个封装起来, 并且使它们可相互替换。此模式使得算法的变化可独立于使用它的客户。

	策略模式就是用来封装算法的，但在实践中可以用它来封装几乎任何类型的规则，只要在分析过程中听到需要在不同时间应用不同的业务规则，就可以考虑使用策略模式处理各种变化的可能性。

特点

几个类的主要逻辑相同，只在部分逻辑的算法和行为上稍有区别的情况

有几种相似的行为，或者说算法，客户端需要动态地决定使用哪一种，那么可以使用策略模式，将这些算法封装起来供客户端调用


本例子中：计算费用的结果就是公共功能


##简单工厂模式

###概念
严格的说，简单工厂模式并不是23种常用的设计模式之一，它只算工厂模式的一个特殊实现


###特点

   1.工厂类包含逻辑判断，根据客户端的选择条件，动态实例化 具体产品类，对于客户端来讲，去除了与具体产品的依赖
   
   2.违反开闭原则
   
   3.可以通过协议和继承实现
   
##工厂模式

###概念
定义一个用于创建对象的接口，让子类决定实例化哪一个类，工厂方法使一个类的实例化延迟到其子类。


###特点

1.符合开闭原则.即当有新产品时，只要新建具体产品并继承抽象产品；新建具体工厂继承抽象工厂；而不用修改任何一个类

2.缺点：每次增加一个产品时，都需要增加一个具体类和对象实现工厂，是的系统中类的个数成倍增加，在一定程度上增加了系统的复杂度，同时也增加了系统具体类的依赖。