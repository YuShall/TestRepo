# Feedback #

Test.gwt.xml
-----
* rename-to 属性让java转换为javascript的编译器把对应模组按照重命名之后的名字来处理。编译后的GWT信息存放在test文件下。
* inherits 从指定的模块继承所有的设置。每个GWT工程都必须继承com.google.gwt.user.User,这是核心。
* extend-property 用来定义本地化参数。
* source 指定那些目录下面的内容要通过GWT编译成JavaScript。
* entry-point 指定本GWT应用的入口点类，要写全路径的类名。
* 将TestEP.java代码转化为javascript是根据这个文件的配置来执行的。

TestEP.java
-----
* `Window.alert("Hello world")`是在运行界面时弹出一个对话框。
* TestEP.java中的代码可以转换为javascript。

settings
-----
* settings文件夹中文件是eclipse的设置的相关文件。

MANIFEST.MFT
-----
* 说明了这个程序的版本、JKD版本等，如果想让jar直接运行，创建MANIFEST文件。

web.xml
-----
* web.xml文件用来初始化配置信息。

index.html
-----
* index.html是首页。`<script type="text/javascript" language="javascript" src="test/test.nocache.js"></script>`引入外部js文件，module配置文件中module的属性rename-to可以用来编译后的文件放在test.test目录下，那么编译后的js就在`test/test.nocache.js`。

问题
-----
* GWT code server的cmd界面是否要一直开着？因为我关掉，http://localhost:8080就打不开，而宋旭关掉，却仍然打得开。
* 「Dev Mode On」更新client side的code的原理是什么？
* 在Eclipse中运行程序的整个过程不是很清楚。

