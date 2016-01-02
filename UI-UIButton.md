# 5.UIButton


##### 1.什么是按钮
* UIButton，俗称“按钮”
* 一般情况下，点击某个控件后，会做出相应反应的都是按钮
* 按钮的功能比较多，既能显示文字，又能显示图片，还能随时调整内部图片和文字的位置
![UIButton.png](http://upload-images.jianshu.io/upload_images/328309-c5567ef9c2706edc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 2.UIButton的状态
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
    

##### 3.在main.storyboard中设置按钮的背景图片
* 设置按钮在不同状态下的背景图片
（为了保证高亮状态下的图片正常显示，必须设置按钮的type为custom）
![UIButton在main.storyBoard中.png](http://upload-images.jianshu.io/upload_images/328309-451691b6c8d71687.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 4.按钮的样式
* 实际上，UIButton自带了很多种不同的样式
![btn在storyboard中的样式.png](http://upload-images.jianshu.io/upload_images/328309-30e8c650044baff9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
* 在用代码创建按钮的同时指定按钮样式
    * UIButton *btn = [UIButton buttonWithType:UIButtonTypeCustom]; 
    * UIButtonTypeCustom：无类型，按钮的内容需要自定义
    * UIButtonTypeDetailDisclosure： 
    * UIButtonTypeInfoLight： 
    * UIButtonTypeInfoDark： 
    * UIButtonTypeContactAdd： 

##### 5.UIButton的常见设置

```objc
 设置按钮的文字
 - (void)setTitle:(NSString *)title forState:(UIControlState)state;
 
 设置按钮的文字颜色
 - (void)setTitleColor:(UIColor *)color forState:(UIControlState)state;

设置按钮内部的小图片
 - (void)setImage:(UIImage *)image forState:(UIControlState)state; 

设置按钮的背景图片
 - (void)setBackgroundImage:(UIImage *)image forState:(UIControlState)state;

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

##### 6.UIButton、UIImageView、UILabel的选择

* UIButton特点
    * 既能显示文字，又能显示图片（能显示2张图片，背景图片、内容图片）
    * 长按高亮的时候可以切换图片\文字
    * 直接通过addTarget...方法监听点击


* UIImageView特点
    * 能显示图片，不能直接通过addTarget...方法监听点击


* UILabel
    * 能显示文字，不能直接通过addTarget...方法监听点击

***
* 选取基本原则
    * 仅仅是显示数据，不需要点击，建议选择UIImageView、UILabel
    * 不仅显示数据，还需要监听点击，建议选择UIButton
    * 长按控件后，会改变显示的内容,不用考虑了，选择UIButton（因为UIButton有highlighted这种状态）
    * 同时显示2张图片：背景图片、内容图片,选择UIButton
    * 其实UIImageView、UILabel也可以通过手势识别器来监听

##### 7.基本的讲的也差不多了，看看能不能灵活运用吧
![九宫格.gif](http://upload-images.jianshu.io/upload_images/328309-9813aede5dff5c74.gif?imageMogr2/auto-orient/strip)


* 需求分析
    * 一开始的界面，只有“添加按钮”可以被点击
    * 点击“添加按钮”，添加内容(白色的实际上是按钮)，同时“删除按钮”可以被点击
    * 在紫色的视图中，“白色按钮”达到6个之后，“添加按钮”再也不能被点击了
    * 当白色按钮全部删除之后，“删除按钮”不能被点击

* 关键点：有规律的创建白色按钮

```objc
ViewController.m文件中
#import "ViewController.h"

// 水平间距
#define hMargin 30
// 垂直间距
#define vMargin 20
// 购物车中按键的高和宽
#define shopBtn 60



@interface ViewController ()

// 添加按钮
@property (nonatomic, strong) UIButton *addBtn;
// 删除按钮
@property (nonatomic, strong) UIButton *delBtn;
// 购物车视图
@property (nonatomic, strong) UIView *shopCarView;

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    
    
    // 1.创建添加按钮
    UIButton *addBtn = [UIButton buttonWithType:UIButtonTypeCustom];
    addBtn.frame = CGRectMake(40, 100, 40, 40);
    [addBtn setBackgroundImage:[UIImage imageNamed:@"add"] forState:UIControlStateNormal];
    [addBtn setBackgroundImage:[UIImage imageNamed:@"add_highlighted"] forState:UIControlStateHighlighted];
    [addBtn setBackgroundImage:[UIImage imageNamed:@"add_disabled"] forState:UIControlStateDisabled];
    
    // 将属性赋值给addBtn
    self.addBtn = addBtn;
    // 既然是按钮，那当然点击按钮之后能有操作了，那就运用播放音乐吧
    /**
     *  添加监听方法
     *
     *  addTarget: 监听对象，一般是填写self
     *  actiong: 调用的方法
     *  forControlEvents: 点击方式
     */
    //    [btn addTarget:<#(nullable id)#> action:<#(nonnull SEL)#> forControlEvents:<#(UIControlEvents)#>]
    // 点击添加按钮的监听
    [addBtn addTarget:self action:@selector(addBtnClick:) forControlEvents:UIControlEventTouchUpInside];
    
    
    // 2.添加删除按钮
    UIButton *delBtn = [UIButton buttonWithType:UIButtonTypeCustom];
    delBtn.frame = CGRectMake(295, 100, 40, 40);
    [delBtn setBackgroundImage:[UIImage imageNamed:@"remove"] forState:UIControlStateNormal];
    [delBtn setBackgroundImage:[UIImage imageNamed:@"remove_highlighted"] forState:UIControlStateHighlighted];
    [delBtn setBackgroundImage:[UIImage imageNamed:@"remove_disabled"] forState:UIControlStateDisabled];
    // 初始的删除按钮要设置成Disabled
    delBtn.enabled = NO;
    
    // 将属性赋值给delBtn
    self.delBtn = delBtn;
    // 点击删除按钮的监听
    [delBtn addTarget:self action:@selector(delBtnClick:) forControlEvents:UIControlEventTouchUpInside];
    
    
    
    // 3.添加一个view，可以放上其他的btn
    UIView *view = [[UIView alloc] init];
    view.frame = CGRectMake(40, 180, 295, 300);
    view.backgroundColor = [UIColor purpleColor];
    
    // 将属性赋值给shopCarView
    self.shopCarView = view;
    
    // 添加两个按钮，view到视图
    [self.view addSubview:addBtn];
    [self.view addSubview:delBtn];
    [self.view addSubview:view];
}

// 点击添加按钮
- (void)addBtnClick:(UIButton *)sender
{
    // 在哪一列
    NSInteger rowTemp = self.shopCarView.subviews.count % 3;
    // 在哪一行
    NSInteger columnTemp = self.shopCarView.subviews.count / 3;
    // 创建btn
    UIButton *shopCarBtn = [UIButton buttonWithType:UIButtonTypeCustom];
    // 设置btn的颜色
    shopCarBtn.backgroundColor = [UIColor whiteColor];
    // 设置每个btn的frame
    shopCarBtn.frame = CGRectMake((hMargin + (hMargin + shopBtn)*rowTemp), (vMargin + (vMargin+shopBtn)*columnTemp), shopBtn, shopBtn);
    // 添加到shopCarView中
    [self.shopCarView addSubview:shopCarBtn];
    
    // 当有六个按钮的时候，就不能再添加了
    if (self.shopCarView.subviews.count == 6) {
        self.addBtn.enabled = NO;
    }
    
    // 恢复删除按钮的使用
    self.delBtn.enabled = YES;
}

// 点击删除按钮
- (void)delBtnClick:(UIButton *)sender
{
    // 删除视图中的最后一个
    UIView *lastShopView = [self.shopCarView.subviews lastObject];
    [lastShopView removeFromSuperview];
    
    // 恢复添加按钮的使用
    self.addBtn.enabled = YES;
    
    if (self.shopCarView.subviews.count == 0) {
        self.delBtn.enabled = NO;
    }
    
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}

@end

```

##### 8.知识点补充
* 有时图层很多，把自己搞懵圈了，可以通过以下一个调试，查看自己的UI图层
![查看图层.png](http://upload-images.jianshu.io/upload_images/328309-bb1b6975731c95b5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)