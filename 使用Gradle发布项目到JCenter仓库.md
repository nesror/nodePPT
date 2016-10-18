title: 使用Gradle发布项目到JCenter仓库
speaker: nestor
url: http://blog.yzapp.cn
transition: slide2
files: /js/demo.js,/css/demo.css,/js/zoom.js
theme: moon
usemathjax: yes

[slide]
# 使用Gradle发布项目到JCenter仓库
## Nestor
2016.09.29

[slide]
## 申请Bintray账号
----
* https://bintray.com/


[slide]
## 添加自动化maven打包插件
----
* 项目的build.gradle（项目最外层的build.gradle文件）增加
````
    // 自动化maven打包插件
    classpath 'com.github.dcendents:android-maven-gradle-plugin:1.5'
````

[slide]

## module的build.gradle里配置POM.xml
----
* 项目的build.gradle（项目最外层的build.gradle文件）增加
````
...
apply plugin: 'com.github.dcendents.android-maven'
...
version = "0.0.3"
...
````
* ![](https://github.com/nesror/nodePPT/blob/master/img/img1.png?raw=true)

[slide]

## 配置源码和javaDoc(可选)
----
* ![](https://github.com/nesror/nodePPT/blob/master/img/img2.png?raw=true)

[slide]
## 生成lib
----
* 这一步为止，就可以生成你项目了，所以我们可以通过如下命令执行生成:
* gradlew install

[slide]
# 增加上传到JCenter的支持
----
* 项目的build.gradle（项目最外层的build.gradle文件）增加
````
    // jfrog上传插件
    classpath "com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.1"
````

[slide]
## 配置你的bintray账号信息
----
* 在你的项目的根目录上的local.properties文件里（一般这文件需gitignore，防止泄露账户信息）配置你的bintray账号信息
* ![](https://github.com/nesror/nodePPT/blob/master/img/img3.png?raw=true)

[slide]
## 配置上传信息
----
````
...
apply plugin: 'com.jfrog.bintray'
...
version = "1.6.4"
...
````
* ![](https://github.com/nesror/nodePPT/blob/master/img/img4.png?raw=true)

[slide]
## 上传，申请添加到JCenter
----
* 执行如下命令完成上传：
* gradlew bintrayUpload

* 申请添加到JCenter
* https://bintray.com/bintray/jcenter ,输入你的项目名字点击匹配到的项目，然后写一写Comments再send即可，工作时间内1小时内就会批准
可能会检查 “def siteUrl = 'https://github.com/nesror/supertextview/ 项目的主页 ”里的项目来确认

[slide]
# 资源前缀
----
* 作用强制在所有资源文件上加上前缀，避免不同aar之间的资源名称冲突，强烈使用！！
* ![](https://github.com/nesror/nodePPT/blob/master/img/img5.png?raw=true)
* ![](https://github.com/nesror/nodePPT/blob/master/img/img6.png?raw=true)
* ![](https://github.com/nesror/nodePPT/blob/master/img/img7.png?raw=true)

[slide]
# 可能遇到的问题
----
* 生成javaDoc报错：
````
  javaDoc注释中有中文：
  注释中非javadoc中规定的注解： 如（以下只有@author是可以用的）：
  /**
       @author: nestor
       @time: 4/9 009-11:56.
       @email: nestor@yzapp.cn
       @desc:
  */
````
* 可以参考这篇博客：
http://blog.yzapp.cn/%E4%BD%BF%E7%94%A8Gradle%E5%8F%91%E5%B8%83%E9%A1%B9%E7%9B%AE%E5%88%B0JCenter%E4%BB%93%E5%BA%93.html

[slide]
# 3步分享你的lib--jitPack

[slide]
## 配置jitPack
----
* ![](https://github.com/nesror/nodePPT/blob/master/img/img8.png?raw=true)
* ![](https://github.com/nesror/nodePPT/blob/master/img/img9.png?raw=true)

[slide]
## 上传到github（可选打release版本）
----
* ![](https://github.com/nesror/nodePPT/blob/master/img/img10.png?raw=true)

[slide]
## 使用
----
* https://jitpack.io/#你的gitHub地址
* ![](https://github.com/nesror/nodePPT/blob/master/img/img11.png?raw=true)
* ![](https://github.com/nesror/nodePPT/blob/master/img/img12.png?raw=true)