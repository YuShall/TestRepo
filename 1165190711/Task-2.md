# Feedback #

Test.gwt.xml
-----
* <module rename-to="test"> rename-to重命名模块，这个属性可以让JAVA->JavaScript的编译器把对应模组按照重命名之后的名字来处理。
	* <inherits name="logical-module-name" /> module类名
	* <extend-property name="locale" values="zh_CN"/> 可用于国际化 
	* <source path="client" /> 每个<source>标签都通过合并其所指定的路径到模块配置XML文件所指定的包中去的方法，加入了一个包到编译器的源码路径内。所有出现在包中的java文件或者其子包都会被编译。
	* <entry-point class="com.dtc.test.client.TestEP" /> module类所在路径
	* <stylesheet src="reset.css" /> 在中用模块的主页中引入css文件或者文件夹，这个效果等同于你在HTML页面中使用script。
	* <add-linker name="xsiframe" />
	* <collapse-all-properties />	
* </module>


TestEP.java
-----
* public class TestEP implements EntryPoint {
*	@Override
*	public void onModuleLoad() {
*		Window.alert("Hello World"); 開啟 browser，輸入網址 http://localhost:8080/TestEP，弹出“hello world”对话框
*	}
*}

web.xml
-----
* web.xml文件用来初始化配置信息。

index.html
-----
* index.html是首页。`<script type="text/javascript" language="javascript" src="test/test.nocache.js"></script>`引入外部js文件，把test/test.nocache.js文件的内容加载到页面中来，所以无论是直接写在页面中的，还是从外部引用的，都可以直接调用里面的方法。

问题
-----
* GWT code server的cmd界面是否要一直开着？因为我关掉，http://localhost:8080就打不开，而宋旭关掉，却仍然打得开。
* 「Dev Mode On」更新client side的code的原理是什么？
* 在Eclipse中运行程序的整个过程不是很清楚。
心得
-----
    觉得有必要解释一下为什么会多出settings、MANIFEST.MFT和内容会和Crystally一样。
    今天的收获还是很多的，但是一直由于网络问题，GPE 不能install（这个问题我昨天在微信群里问过，公司网络限速也更新不了，是在回寝室才能翻墙install）。然后，我一直用的是Maven 啟動 Tomcat 7的，没有用ecplise，而且不知道为什么，是有setting这个文件的（现在还是有的）。查找的资料也有setting文件和介绍，Crystally也给我看过她的，也和百度到的类似，所以就根据资料看了一下就上传了。
    我知道确实是有些地方偷懒了，也请老师能帮我们解决问题，谢谢。

