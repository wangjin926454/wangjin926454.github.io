## Welcome to wangjin926454's GitHub Pages


### Markdown

```markdown
Syntax highlighted code block

# java核心卷2
##第一章 Java SE 8的流库
    流:说明我们想要什么样的结果，而不是如何实现得到结果
    处理流时是并行处理但不是多线程
    示例见:https://github.com/wangjin926454/java_volume_1/tree/master/java_volume_2_1/stream
    API见:java.util.stream   java.util.Optional<T>


# Effective Java
##第一条 考虑用静态工厂方法代替构造函数
  ·好处1：与构造函数不同、静态工厂方法具有名字，能更确切地描述作用、更易于使用
  ·好处2：1）与构造函数不同，每次被调用的时候，不要求非得创建一个新的对象。对于非可变类、
		可以使用一个预先构造好的实例缓存起来，避免重复对象。类似单例模式。
	   2）使非可变类不会有两个相等的实例存在。即当且仅当a==b的时候才有a.equals(b)为true
		那么客户端可以用==操作符来代替equals(Object)方法
  ·好处3：静态工厂方法可以返回一个原类型的子类型的对象。例如在Collections中，一个API可以返回一个对象
		同时又不使该对象的类成为公有的。

##第二条 使用私有构造函数强化singleton属性
  	   1）在创建单例模式的时候，构造函数使用private、保证唯一实例对象只能通过getInstance()方法获得
	   2）为了使一个singleton类变成可序列化的(serializable)，仅仅在类中"implements Serializable"是
		不够的，为了维护singleton方法，必须提供一个readResolve方法。从内存读出而组装的对象破坏
		了单例的规则。单例是要求一个JVM中只有一个类对象的，而现在通过反序列，一个新的对象克隆了
		出来。违反的单例的原则.使用readResolve方法，当JVM从内存中反序列化地"组装"一个新对象时，
		就会自动调用这个 readResolve方法来返回指定的对象。

##第三条 通过私有的构造函数强化不可实例化的能力
	   1）不希望工具类实例化也防止工具类被实例化。最好的办法是提供一个私有的构造函数来防止工具类被实例化。


##第四条 避免创建重复的对象
	   1）在某些对象初始化之后不会改变时、尽量避免重复创建对象。使其作为static块和static final常量。

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```
### Support or Contact

