title: kotlin初步使用
speaker: nestor
url: https://github.com/ksky521/nodePPT
transition: slide2
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: moon
usemathjax: yes

[slide]
# Kotlin
## 哈哈哈哈哈
我曾经尝试用 Scala 写了个 Android 的 HelloWorld，一切都配置好以后，仅仅引入了 Scala 常见的几个库，加上 support-v4 以及 appcompat 这样常见的库，结果还是报错了。是的，65K。。。而且用 Scala 开发 Android 的话，基于 gradle 的构建会让整个 app 的 build 过程异常漫长，有时候你会觉得自己悟出了广义相对论的奥义，哦不，你一定是晕了，时间并没有变慢。

相比之下，Kotlin 的标准库只有 7000 个方法，比 support-v4 还要小，这正反映了 Kotlin 的设计理念：100% interoperable with Java。其实我们之前就提到，Java 有的 Kotlin 就直接拿来用，而 Scala 的标准库要有 5W 多个方法，想想就还是想想算了

[slide]
# 为什么要引入kotlin
* 

[slide]
# 使用
*  
    > ![](https://github.com/nesror/nodePPT/blob/master/img/kotlin3.jpg?raw=true)
    > ![](https://github.com/nesror/nodePPT/blob/master/img/kotlin4.jpg?raw=true)

[slide]
# 类,基本语法,与Java对比
----
* Kotlin
    > ![](https://github.com/nesror/nodePPT/blob/master/img/kotlin1.jpg?raw=true)
* Java
    > ![](https://github.com/nesror/nodePPT/blob/master/img/kotlin2.jpg?raw=true)
* 其他基本用法（list等）详见：
    > <https://nesror.gitbooks.io/kotlin/content/>

[slide]
# 扩展函数

[slide]
# null安全

[slide]
# Android Extensions
> nodePPT 让每个人都爱上做分享！

[slide]
# 委托
----
标准委托

       Kotlin 的标准库中已经内置了很多工厂方法来实现属性的委托。

lazy

       lazy 用于进行惰性加载，即第一次使用时才执行初始化的操作。

Observable

       observable 可以用于实现观察者模式。
NotNull

       notNull 适用于那些无法在初始化阶段就确定属性值的场合。
以 Map 形式保存属性的值

       Kotlin 中有一种特别的委托，可以以 Map 作为一个类的构造方法的参数，访问该类的属性就是访问该 Map 的键值对。这种做法非常类似 Groovy 中的带名构造方法。 
要实现这一功能需要得意于 Kotlin 内置的属性的扩展方法 kotlin.properties.getValue 

[slide]
# 风险，难点

对比包大小，方法数
委托的坑
开发风险，对现在项目的意义
熟悉之后会提升开发效率
----