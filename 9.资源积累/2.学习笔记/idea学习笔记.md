## idea学习笔记

----

### idea下载

> 下载官网
>
> > `http://www.jetbrains.com/idea/download/#section=windows`
>
> Ultimate
>
> > 旗舰版
> >
> > > 用于web和企业开发
>
> > windows JBR 8	---- 基于jdk8开发
> >
> > windows JBR 11	---- 基于jdk11开发
> >
> > 。。。。。。 
>
> Community
>
> > JVM和Android开发



### 对idea进行配置

> 目录地址
>
> > `D:\software\idea\IntelliJ IDEA 2019.3\bin`
>
> 文件名
>
> > `idea.exe.vmoptions`
> >
> > > `-Xms128m`	初始堆的大小
> > >
> > > `-Xmx512m`	最大堆的大小
> > >
> > > .......
>

#### 运行内存及编码配置

> Help ---> Edit Custom Options ...
>
> > `-Xms128m`	初始堆内存的大小
> >
> > `-Xmx4096m`	最大堆内存的大小
> >
> > `-Dfile.encoding=UTF-8`	强制系统文件编码格式为utf-8，可能会与window的bgk产生冲突
> >
> > > Edit Configurations --> Tomcat Server --> Tomcat8 --> VM options
> > >
> > > > `-Dfile.encoding=UTF-8`

#### 热更新配置

> Edit Configurations --> Tomcat Server --> Tomcat8
>
> > `On 'Update' action`
> >
> > > `Update class and resourses`
> >
> > `On frame deactivation`
> >
> > > `Update class and resourses`

#### 传参出错可能需要的配置

> `https://www.jianshu.com/p/64e6e91a49c0`



#### Idea的基本设置

##### 外观设置

> File ---> Settings
>
> > `Appearance & Behavior`		-外观行为
> >
> > `Keymap`		-快捷键
> >
> > `Editor`		-编辑器
> >
> > `Plugins`		-插件
> >
> > `Version Controller`		-版本控制
> >
> > `Builder，Execution，Deployment`		-构建，执行，部署
> >
> > `Languages & Frameworks`		-语言，框架
> >
> > `Tools`		-工具

##### 鼠标滑轮修改字体大小

> Editor ---> General ---> Change font size(Zoom) with Ctrl+Mouse Wheel (勾选)

##### 鼠标悬浮提示

> Editor ---> General ---> show quick documentation on mouse move (勾选)

##### 自动导包功能

> Editor ---> General ---> Auto Import
>
> > 勾选
> >
> > > Add unambiguous imports on the fly
> > >
> > > Optimize imports on the fly (for current project)

##### 显示代码行号和方法间的分隔符(默认勾选)

> Editor ---> General ---> Appearance
>
> > 勾选
> >
> > > Show line numbers	-显示行号
> > >
> > > Show method separators	-方法分隔符

##### 忽略大小写提示

> Editor ---> General ---> Code Completion ---> Match case(取消勾选)

##### 文件多行显示

> Editor ---> General ---> Editor Tabs ---> Show tabs in one row (取消勾选)

##### 字体设置

###### 默认字体，字体大小，行间距

> Editor ---> font
>
> > Font		-修改字体
> >
> > Size		-修改字体大小
> >
> > Line spacing	-修改行间距

###### 代码编辑区字体大小	

> Editor ---> Color Scheme ---> Color Scheme Font
>
> > 保存过后与上方配置一致

###### 控制台输出的字体和字体大小

> Editor ---> Console Scheme ---> Console Font

###### 修改单行,多行,文档注释的字体颜色

> Editor ---> Color Scheme ---> Language Defaults ---> Comments
>
> > `Block comment`	-多行注释
> >
> > `Doc Comment ---> Text`	-文档注释
> >
> > `Line Comment`	-单行注释

##### 工程项目编码设置	

> Editor ---> File Encodings
>
> > Global Encoding	-全局编码
> >
> > Project Encoding	-当前项目编码
> >
> > Projecties Files(*.properties)	-属性文件编码

> 还可以在idea的右下方设置单个文件的编码

##### idea自动编译设置

> idea默认不会自动编译

> Build，Execution，Deployment ---> Compiler
>
> > 勾选
> >
> > > Builder project automatically
> > >
> > > Compile independent modules in parallel



### view

> Appearance	--->	Toolbar
>
> > 显示快捷栏
> >
> > > 打开文件，保存，刷新和配置......



### 快捷键

#### 查找快捷键

> Keymap ---> 放大镜(符号) ---> 输入想要查找的快捷方式

#### 修改快捷键

##### 代码提示自动补全

> Keymap ---> Basic(搜索) 
>
> > Remove *	-先移除
> >
> > Add Keyboard Shortcut	-再添加新的快捷键

#### 常用快捷键

##### 代码自动生成

###### `Alt + /`		-代码自动补全(手动设置)

###### `alt + insert`		-生成构造，get()，set()方法等

###### `ctrl + shift + 回车`		-补全结尾

###### `ctrl + j`		-自动代码生成模板

> `psnm`		-生成main方法
>
> `fori`		-生成for循环
>
> `sout`		-println输出

###### `ctrl + alt + t`		-将选中代码自动放入到if，for....中

> 使用该快捷键时需要将qq关闭

###### `ctrl + alt + v` ---> `alt + shift + l`		-生成返回值对象

###### ？.for		-对？进行增强for循环



##### 代码格式优化

###### `ctrl + alt + l`		-代码格式优化

> 需要关闭QQ相关快捷键



##### 代码编辑

###### `ctrl + y`		-删除行

###### `ctrl + d`		-复制行

###### `ctrl + w`		-自动选中代码

###### `ctrl + g`		-跳转到指定行



##### debug调试

> 在行号栏直接点击进行断点的设置
>
> 以debug的方式运行程序



##### 查询快捷键

###### `ctrl + n`		-查找类

###### `ctrl + f`		-查找当前页面文本

###### `ctrl + r`		-当前扣扣文本替换



##### 其他快捷键

###### `ctrl + z`		-后退

###### `ctrl + /`		-单行注释





### idea模板使用

##### 实时代码模板（Live Templates）

> File ---> Settings ---> Editor ---> Live Templates

> 例如
>
> > output
> >
> > > serr 
> > >
> > > sout 
> > >
> > > ...
>
> 也可以自己设置模板
>
> > `System.out.println("$VAR1$值="+$VAR1$,"$VAR2$值="+$VAR2$);$END$`
> >
> > > 模板需要手动设置使用范围才能够使用

##### 文件和代码模板（File and Code Templates）

> File ---> Setting ---> File and Code Templates
>
> 一般不使用

##### postfix模板

> File ---> Setting ---> Editor ---> General ---> Postfix Completion

> 例如
>
> > `for`
> >
> > `fori`
> >
> > .....



### IDEA中Maven的配置

##### 在idea中配置JDK

> File ---> Project Structure
>
> > SDKs		-SDK的全局配置，没有的话需要添加
>
> > Project		-SDK的项目配置
> >
> > > 也可以在此设置项目的编译输出路径

##### 下载Maven，配置Maven环境

> 修改Maven的`settings.xml`配置文件,配置默认的地址，和镜像地址

###### idea配置Maven

> File ---> Setting ---> Build,Execution,Deployment ---> Build ---> Maven
>
> > Maven home directory 	-进行配置
>
> Maven ---> Importing
>
> > Import Maven projects automatically(勾选)

> Maven全局配置
>
> > File ---> Other Settings ---> Setting for New Projects ---> Maven





##### 创建一个Maven项目

> File ---> New Project ---> Maven ---> Create from archetype(勾选) ---> maven-archetype-quickstart

##### 对Maven项目进行打包

> 选择idea左下方`Terminal`
>
> > 输入命令
> >
> > > `mvn clean package`
> > >
> > > > 在target目录下就会出现相关jar包
>
> 运行jar包
>
> > `C:\Users\asus\IdeaProjects\untitled>java -cp target/untitled-1.0-SNAPSHOT.jar org.example.App`



##### Maven组件界面介绍

> 在Maven项目的右侧



##### Maven快速排查依赖包冲突

> 打开`pom.xml`,右击 ---> Diagrams ---> show dependencies
>
> > 会显示包的关系图
> >
> > > 如果有红色虚线，则代表有冗余jar包
> > >
> > > > 此时可以点击冲突包的右键 ---> exclude(将多余的包排除掉)





### 对一般项目进行打包

> File ---> Project Structure ---> Artifacts ---> + ---> JAR(添加需要打包的项目) ---> 选中jar包 ---> apply ---> ok
>
> Build ---> Build Artifacts ---> *.jar ---> Build
>
> > 在项目的out目录下可以找到jar包

> 单独运行jar包指令
>
> > `java -cp *.jar package.class`
> >
> > > `java -cp jar包名称 包名.类名`





### idea导入eclipse项目

##### idea导入eclipse项目

> idea支持直接打开eclipse项目
>
> > File ---> Open ---> 选择项目的`.project`文件 ---> Open as Project
>
> > 如果报错，手动刷新项目即可

##### idea对项目目录类型手动标注

> 右击所要选择的目录 ---> Mark Direxctory as
>
> > Test Sources Root
> >
> > > 标注可编译的单元测试的目录
> >
> > Resourses Root
> >
> > > 标注资源文件目录
> >
> > Test Resources Root
> >
> > > 标注单元测试资源目录
> >
> > Excluded
> >
> > > 标注排除目录
> > >
> > > > 这个目录中的代码不会进行资源检查会被排除掉
> >
> > Generated Sources Root 
> >
> > > 标记src中的java目录，只有这个目录才可以新建类和包



##### idea创建resourse资源目录

> File ---> Peoject Structure ---> Modules
>
> > 右击src下的main文件夹 ---> 新建一个resources目录
> >
> > 右击resourcs ---> 选择Resources
>
> resources文件夹，放置配置文件等信息



##### idea创建并读取properties文件

> 右击resources ---> new ---> Resource Bundle ---> 给文件起名





### idea创建多Module项目

##### idea创建多Module项目

> File ---> new ---> Project ---> 直接next ---> 输入相关信息创建成功
>
> > 创建子模块
> >
> > > 右击已建好的项目 ---> New ---> Module ---> 直接next ---> 输入相关信息创建成功



##### idea设置Module之间的依赖关系

> File ---> Project Structure ---> Modules
>
> > 点击项目 ---> Dependencies ---> + ---> Module Dependency ---> 添加项目
> >
> > > 表示添加的项目依赖于前面的项目
> >
> > > 之后还需要在添加的项目的配置文件中添加依赖



##### idea多Module调用

> 依赖的包之间的方法可以互相调用





### idea创建集成Tomcat

##### idea构建Tomcat项目

> File ---> New ---> Project ---> Maven ---> Create from archetype(勾选) ---> webapp ---> 填写信息直到创建成功

##### idea创建Maven Web项目目录

> File ---> Project Structure ---> Modules
>
> > src ---> 右击main ---> New Folder 
> >
> > > java(创建文件夹的名称)
> > >
> > > > 右击java ---> Sources
> > >
> > > resources(创建文件夹的名称)
> > >
> > > > 右击resources ---> Resources

> java ---> New ---> Package ---> 输入包名
>
> resources ---> New ---> Resource Bundle ---> 输入配置文件名称



##### idea集成Tomcat

>   Add Configuration ---> Tomcat Server ---> Local
>
>   > Server ---> Application server(找到提前下载的Tomcat目录) ---> 配置默认浏览器，jre等信息
>
>   详细百度





### idea使用Maven构建Scala

##### windows下scala环境配置

> 先去官网下载scala.msi进行自动化安装
>
> > 在Scala课前资料中已有2.11.7版本

##### idea安装scala插件

>  Configure ---> Plugins ---> Scala



### idea进行单元测试

> `https://blog.csdn.net/VinsmS/article/details/80858944`







### 好用的插件

##### `Translation`

> `ctrl+shift+y`翻译，`ctrl+shift+s`切换翻译源

##### `Free MyBatis plugin`

##### `lombok`

> 使用lombok时，会出现get，set提示

