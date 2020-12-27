# maven

## 什么是maven
Maven 翻译为"专家"、"内行"，是 Apache 下的一个纯 Java 开发的开源项目。基于项目对象模型（缩写：POM）概念，Maven利用一个中央信息片断能管理一个项目的构建、报告和文档等步骤。
Maven 是一个项目管理工具，可以对 Java 项目进行构建、依赖管理。Maven 也可被用于构建和管理各种项目。

约定配置
Maven 提倡使用一个共同的标准目录结构，Maven 使用约定优于配置的原则，大家尽可能的遵守这样的目录结构。如下所示：

目录	目的
${basedir}	存放pom.xml和所有的子目录  
${basedir}/src/main/java	项目的java源代码  
${basedir}/src/main/resources	项目的资源，比如说property文件，springmvc.xml  
${basedir}/src/test/java	项目的测试类，比如说Junit代码  
${basedir}/src/test/resources	测试用的资源  
${basedir}/src/main/webapp/WEB-INF	web应用文件目录，web项目的信息，比如存放web.xml、本地图片、jsp视图页面  
${basedir}/target	打包输出目录  
${basedir}/target/classes	编译输出目录  
${basedir}/target/test-classes	测试编译输出目录  
Test.java	Maven只会自动运行符合该命名规则的测试类   
~/.m2/repository	Maven默认的本地仓库目录位置  

## Maven POM
POM( Project Object Model，项目对象模型 ) 是 Maven 工程的基本工作单元，是一个XML文件，包含了项目的基本信息，用于描述项目如何构建，声明项目依赖，等等。
执行任务或目标时，Maven 会在当前目录中查找 POM。它读取 POM，获取所需的配置信息，然后执行目标。
POM 中可以指定以下配置：
项目依赖  
插件  
执行目标  
项目构建 profile  
项目版本  
项目开发者列表  
相关邮件列表信息  

## 父（Super）POM
父（Super）POM是 Maven 默认的 POM。所有的 POM 都继承自一个父 POM（无论是否显式定义了这个父 POM）。父 POM 包含了一些可以被继承的默认设置。因此，当 Maven 发现需要下载 POM 中的 依赖时，它会到 Super POM 中配置的默认仓库 http://repo1.maven.org/maven2 去下载。

Maven 使用 effective pom（Super pom 加上工程自己的配置）来执行相关的目标，它帮助开发者在 pom.xml 中做尽可能少的配置，当然这些配置可以被重写。


