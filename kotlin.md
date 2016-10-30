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
----