#Sky — Dart for Android

##1. Dart介绍

Dart刚开始是用来设计代替Javascript设计webApp的语言。其语法大量借鉴的Java和JavaScript。[中文网站](http://www.dartlang.cc/)
 

##2. Dart语法

中文网站 [step by step](http://www.dartlang.cc/codelabs/darrrt/)
	


##3. Sky与Dart的关系

Sky uses Dart and Sky applications are [Dart Packages](https://www.dartlang.org/docs/tutorials/shared-pkgs/).

##4. Sky内核

The Sky engine. The engine is the core of the system. Written in C++, the engine provides the muscle of the Sky system. The engine provides several primitives, including a soft real-time scheduler and a hierarchial, retained-mode graphics system, that let you build high-quality apps.

Sky引擎。这个引擎是用C++写的，是Sky系统的核心，提供了Sky系统的基础功能，包括实时调用，和一套分层的，retained-mode(保留模式？)的图形界面系统。让开发人员能够开发高质量的apps

The Sky framework. The framework makes it easy to build apps using Sky by providing familiar user interface widgets, such as buttons, infinite lists, and animations, on top of the engine using Dart. These extensible components follow a functional programming style inspired by React.

Sky框架。这个框架让应用的编写变的简单。框架用Dart基于Sky引擎编写，提供了开发人员熟悉的用户界面控件，比如按钮，无限列表，动画等。这些可扩展的组件采用了从React借鉴过来的函数式风格
	
##5. Effen Sky的引擎
Effen is a functional-reactive framework for Sky which takes inspiration from React. Effen is comprised of three main parts: a virtual-dom and diffing engine, a component mechanism and a very early set of widgets for use in creating applications.

Effen是一个functional-reactive(通过函数进行控制？)的框架，也是React的方式。Effen包含三个主要部分：一个虚拟的dom树和diffing引擎，一个component机制和一系列比较粗糙的widget供用户开发应用
	
##6. 一个简单的Demo — Hello World
	
	// In main.Sky
	<script>
	import 'hello_world.dart';

	main() {
	  new HelloWorldApp();
	}
	</script>

----------

	// In hello_world.dart
	import 'package:Sky/framework/fn.dart';

	class HelloWorldApp extends App {
		 UINode build() {
	    return new Text('Hello, world!');
	  }
	}
注： UINode是Sky的framework的一个组件基类，hello_world.dart的主要作用是构造一个Text组件（间接继承UINode）

##7. 另一个Demo — stock

[stock](https://github.com/domokit/sky_sdk/tree/master/examples/stocks)


##8. 组件

目前可用的UI组件只有
├── action_bar.dart
├── animated_component.dart
├── button_base.dart
├── button.dart
├── checkbox.dart
├── drawer.dart
├── drawer_header.dart
├── fixed_height_scrollable.dart
├── floating_action_button.dart
├── icon_button.dart
├── icon.dart
├── ink_splash.dart
├── ink_well.dart
├── input.dart
├── material.dart
├── menu_divider.dart
├── menu_item.dart
├── modal_overlay.dart
├── popup_menu.dart
├── popup_menu_item.dart
├── radio.dart
├── scaffold.dart
└── scrollable.dart
还有Text，在../fn.dart里。fn.dart里声明了UI组件的基类。

还有一些动画相关的组件，相关资料都欠缺，有兴趣的自己去framework里面查看[源代码](https://github.com/domokit/sky_sdk/tree/master/packages/sky/lib/framework)


##9. 结论 


> Written with [Larry](http://ckitterl.blogspot.com/).
