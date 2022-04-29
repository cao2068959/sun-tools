# 1. 简介

该包是 JDK8下`sun tools.jar`的一个maven代理包

在`jdk9` 之前要使用`tools`中的内容需要, 自己从本地导入, 并没有提供对应的maven坐标如:
```xml
<dependency>
    <groupId>com.sun</groupId>
    <artifactId>tools</artifactId>
    <version>1.8</version>
    <scope>system</scope>
    <systemPath>${project.basedir}/src/main/resources/lib/tools.jar</systemPath>
</dependency>

```
使用上述方式导入项目, 会导致最终打包出现一定问题.

所以本库提供了maven坐标的方式去引用 JDK8下的`sun tools.jar`包

# 2.使用方法

> 仅仅只提供 JDK8下的的`tools`, 因为高JDK版本的 `tools` 已经继承到jdk-sdk中, 可以直接在项目中通过导入模块的方式使用

```xml
<dependency>
    <groupId>io.github.cao2068959</groupId>
    <artifactId>sun-tools</artifactId>
    <version>8</version>
</dependency>
```

