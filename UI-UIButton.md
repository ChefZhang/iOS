# UIButton

## 1.什么是按钮
* UIButton，俗称“按钮”
* 一般情况下，点击某个控件后，会做出相应反应的都是按钮
* 按钮的功能比较多，既能显示文字，又能显示图片，还能随时调整内部图片和文字的位置
![UIButton.png](http://upload-images.jianshu.io/upload_images/328309-c5567ef9c2706edc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 2.UIButton的状态
* normal（普通状态）
    * 相当于可以点击该按钮，但是没有点击 
    * 默认情况（Default）
    * 对应的枚举常量：UIControlStateNormal
* highlighted（高亮状态）
    * 按钮被按下去的时候（手指还未松开）
    * 对应的枚举常量：UIControlStateHighlighted
* disabled（失效状态，不可用状态）
    * 如果enabled属性为NO，就是处于disable状态，代表按钮不可以被点击
    * 对应的枚举常量：UIControlStateDisabled
    

### 3.在main.storyboard中设置按钮的背景图片
* 设置按钮在不同状态下的背景图片
（为了保证高亮状态下的图片正常显示，必须设置按钮的type为custom）
![UIButton在main.storyBoard中.png](http://upload-images.jianshu.io/upload_images/328309-451691b6c8d71687.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 4.按钮的样式
* 实际上，UIButton自带了很多种不同的样式
![btn在storyboard中的样式.png](http://upload-images.jianshu.io/upload_images/328309-30e8c650044baff9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 在用代码创建按钮的同时指定按钮样式
    * UIButton *btn = [UIButton buttonWithType:UIButtonTypeCustom]; 
    * UIButtonTypeCustom：无类型，按钮的内容需要自定义
    * UIButtonTypeDetailDisclosure： 
    * UIButtonTypeInfoLight： 
    * UIButtonTypeInfoDark： 
    * UIButtonTypeContactAdd： 

### 5.UIButton的常见设置
```objc
 设置按钮的文字
 - (void)setTitle:(NSString *)title forState:(UIControlState)state;
 
 设置按钮的文字颜色
 - (void)setTitleColor:(UIColor *)color forState:(UIControlState)state;

设置按钮内部的小图片
 - (void)setImage:(UIImage *)image forState:(UIControlState)state; 

设置按钮的背景图片
 - (void)setBackgroundImage:(UIImage *)image forState:(UIControlState)state;

```


```objc
设置按钮的文字字体（需要拿到按钮内部的label来设置）
btn.titleLabel.font = [UIFont systemFontOfSize:13];

获得按钮的文字
- (NSString *)titleForState:(UIControlState)state; 

获得按钮的文字颜色
- (UIColor *)titleColorForState:(UIControlState)state;

获得按钮内部的小图片
- (UIImage *)imageForState:(UIControlState)state;

获得按钮的背景图片
- (UIImage *)backgroundImageForState:(UIControlState)state;

```

