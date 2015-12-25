# adsf

## 2.第一个OC程序
***
### 本节知识点
1. 如何创建Objective-C项目
2. \#import和#include区别
3. NSLog和printf区别
4. "@"的使用方法  
5. NS前缀

***
#### 1.如何创建Objective-C项目
* 创建工程
![](file:/Users/John/Desktop/笔记图片/Snip20150512_3.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20150512_4.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20151225_22.png =490x)
![](file:/Users/John/Desktop/笔记图片/Snip20151225_23.png =490x)

***
#### 2.\#import和#include区别
* \#import和#include的类似，都是把其后面的文件拷贝到该指令所在的地方
* \#import可以自动防止重复导入
* \#import<>用于包含系统文件
* \#import""用于包含本项目中的文件
* \#import告诉编译器找到并处理名为Foundation.h的文件，这是一个系统文件，\#import表示将该文件的信息导入到程序中。
* 框架地址：/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneO S.sdk/System/Library/Frameworks/

***
#### 3.NSLog和printf区别
* NSLog是Foundation框架􏰀供的Objective-C日志输出函数,与标准C中的printf函数类似,并可以格式化输出。

	* NSLog传递进去的格式化字符是NSString的对象,而不是char *这种字符串指针
	* NSLog输出的内容中会自动包含一些系统信息
	* NSLog输出的内容会自动换行
* NSLog声明在NSObjCRuntime.h中
	* 声明：void NSLog(NSString *format, ...);
	
```
NSLog(@“this is a test”); //打印一个字符串
NSString *str = @"hello xiaomage!”;
NSLog(@"string is:%@",str);//使用占位符,%@表示打印一个对象,%@ OC特有的
NSLog(@"x=%d, y=%d",10,20);//使用多个占位符,%d表示整型数
```
***
#### 4."@"的使用方法
* 在OC中"@"有特殊的用法
	* "@"这个符号表示将一个C的字符串转化为OC中的字符串对象NSString
	* OC中大部分的关键字都是以@开头的，比如@interface, @implemention, @end等
***
#### 	5.NS前缀 
* NS来自于NeXTStep的一个软件 NeXT Software
* OC中不支持命名空间(namespace)
* NS是为了避免命名冲突而给的前缀
* 看到NS前缀就知道是Cocoa中的系统类的名称

***
***
## 3.面向对象思想
***
### 本节知识点
1. 面向对象基本概念
2. 面向对象和面向过程区别
3. 面向对象的特点
***
#### 1.面向对象基本概念
* 面向对象(Object Oriented,OO)是软件开发方法
* 面向对象是一种对现实世界理解和抽象的方法，是计算机编程技术发展到一定阶段后的产物。
* Object Oriented Programming-OOP ——面向对象编程

#### 2.面向对象和面向过程区别
* 面向对象是相对面想过程而言
* 面向对象和面向过程都是一种思想
* 面向过程
	* 强调的是功能行为
	* 关注的是解决问题需要哪些步骤
* 面向对象
	* 将功能进行封装，强调具备功能的对象
	* 关注的是解决问题需要哪些对象
	
#### 3.面向对象的特点
* 可以将复杂的事情简单化
* 将程序员从执行者转化为指挥者
* 完成需求时：
	* 先要去找具有所需的功能的对象来用
	* 如果该对象不存在，那么创建一个具有所需功能的对象
	* 这样简化开发并提高复用
	
***
## 类与对象	
