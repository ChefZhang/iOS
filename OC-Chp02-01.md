# 1.NSString类介绍及用法

## 本小节知识点:

* 【掌握】NSString常见方法
* 【掌握】NSString字符串长度计算
***
### 1.NSString常见方法

* NSString是Objective-C 中核心处理字符串的类之一

* 创建常量字符串,注意使用“@“符号。
```objc
NSString *astring = @"This is a String!";
```
* 创建空字符串,给予赋值。
```objc
NSString *string = [NSString new];
string = @"chefzhang";
```
* 创建格式化字符串:占位符(由一个%加一个字符组成)
```objc
[NSString stringWithFormat:@"chefzhang体重%i岁了", 130];
```

### 2.NSString字符串长度计算

* 通过调用NSString类的对象方法 length 可以获得字符串的长度
* 字符串长度是指该字符串中一共有多个字符(无论是中文还是英文)

* 纯英文字符
```objc
    NSString *str = @"tom";
    NSLog(@"length = %i", [str length]);
    输出结果:3
```
    
* 中英文混合
```objc
    NSString *str = @"tom杨";
    NSLog(@"length = %i", [str length]);
    输出结果:4
```

* 纯中文
```objc
    NSString *str = @"杨春福";
    NSLog(@"length = %i", [str length]);
    输出结果:3
```

* NSUInteger 就是 unsigned long
```objc
源码：
typedef unsigned long NSUInteger;
```