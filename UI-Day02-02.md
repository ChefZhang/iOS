# UIImageView

## 1.UIImageView的常用属性
* UIImageView极其常用，功能比较专一：显示图片
 
    * @property(nonatomic,retain) UIImage *image; 
显示的图片

    * @property(nonatomic,copy) NSArray *animationImages; 
显示的动画图片

    * @property(nonatomic) NSTimeInterval animationDuration; 
动画图片的持续时间

    * @property(nonatomic) NSInteger      animationRepeatCount; 
动画的播放次数（默认是0，代表无限播放）

* UIImageView继承自UIImage
    * @interface UIImageView : UIView  
    * 因此拥有图片显示模式的属性contentMode

### 小试牛刀
* 添加图片

![添加图片.png](http://upload-images.jianshu.io/upload_images/328309-5b47c686f1002083.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 代码参考

```objc
    // 1.1 创建UIImageView对象
    UIImageView *imageView = [[UIImageView alloc] init];
    // 1.2 设置frame
    imageView.frame = CGRectMake(0, 0, 200, 300);
    imageView.center = self.view.center;
    // 1.3 设置背景
    imageView.backgroundColor = [UIColor yellowColor];
    // 1.4 设置图片 (png不需要后缀)
    imageView.image = [UIImage imageNamed:@"kb"];
    /**
     UIViewContentModeRedraw, // 重新绘制 (核心绘图) drawRact
     
     //带有Scale,标明图片有可能被拉伸或压缩
     UIViewContentModeScaleToFill, // 完全的压缩或拉伸
     
     // Aspect 比例,缩放是带有比例的
     UIViewContentModeScaleAspectFit, // 宽高比不变 Fit 适应，图片的高度达到imageView的高度
     UIViewContentModeScaleAspectFill, // 宽高比不变 Fill 填充，图片的宽度达到imageView的宽度
     
     //不带有Scale,标明图片不可能被拉伸或压缩
     UIViewContentModeCenter,
     UIViewContentModeTop,
     UIViewContentModeBottom,
     UIViewContentModeLeft,
     UIViewContentModeRight,
     UIViewContentModeTopLeft,
     UIViewContentModeTopRight,
     UIViewContentModeBottomLeft,
     UIViewContentModeBottomRight,
     */
    // 1.5 设置图片的内容模式
    imageView.contentMode = UIViewContentModeScaleAspectFill;
    
    // 是否裁剪多余的部分，这个要配合contentMode使用
//    imageView.clipsToBounds = YES;
    
    // 2.0 加到控制器的view中
    [self.view addSubview:imageView];
```    


* 图片具有毛玻璃效果（应用场景：音乐播放软件）

![毛玻璃效果.png](http://upload-images.jianshu.io/upload_images/328309-3c90247fed93227b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 代码如下
```objc
    // 让图片具有毛玻璃效果
    // 1.创建UIImageView的对象
    UIImageView *imageView = [[UIImageView alloc] init];
    // 2.设置尺寸，铺满整个屏幕
    imageView.frame = self.view.bounds;
    // 3.设置图片
    imageView.image = [UIImage imageNamed:@"kb"];
    // 4.设置图片样式
    imageView.contentMode = UIViewContentModeScaleAspectFill;
    // 5.添加到视图中
    [self.view addSubview:imageView];
    // 6.添加毛玻璃，需要的控件是UIToolBar
    UIToolbar *toolBar = [[UIToolbar alloc] init];
    // 6.1设置尺寸
    toolBar.frame = self.view.bounds;
    // 6.2毛玻璃的样式
    /*
     UIBarStyleDefault          = 0,
     UIBarStyleBlack            = 1,
     */
    toolBar.barStyle = UIBarStyleBlack;

    // 6.3添加到iamgeView图层上
    [imageView addSubview:toolBar];
```   


## 2.UIImageView的常用方法
UIImageView不光可以加载图片，还能播放帧动画 
![lol巨魔.gif](http://upload-images.jianshu.io/upload_images/328309-5d230fd03842aa26.gif?imageMogr2/auto-orient/strip)

听起来是不是很酷炫，那么完成这样就需要以下方法了
* \- (void)startAnimating; // 开始动画
* \- (void)stopAnimating; // 停止动画
* \- (BOOL)isAnimating; // 是否正在执行动画

看下demo吧

* 注意：beginAnimation对应就是播放动画的按钮监听

```objc
- (IBAction)beginAnimation {
    
    // 3.这么写，还是有一个bug，就是连续点击“播放动画”按钮，画面会一直重复播放，改进办法
//    if (self.imageView.isAnimating)
//        return;
    
    
    // 2.为什么创建数组要放在此处呢？ 因为当我不点击这个按钮的时候，我就不需要让动画加载进来，这样就可以节省内存了！
    
    // 1.要播放帧动画，就要创建一个数组
    NSMutableArray<UIImage *> *imageArr = [NSMutableArray array];
    for (int i = 0; i < 20; i++) {
        
        /**
         加载图片的方式:
         1. imageNamed:
         2. imageWithContentsOfFile:
         
         1. 加载Assets.xcassets这里面的图片:
         1> 打包后变成Assets.car
         2> 拿不到路径
         3> 只能通过imageNamed:来加载图片
         4> 不能通过imageWithContentsOfFile:来加载图片
         
         2. 放到项目中的图片:
         1> 可以拿到路径
         2> 能通过imageNamed:来加载图片
         3> 也能通过imageWithContentsOfFile:来加载图片
         */
        
        // 5.如果用imageNamed: 有内存缓存，直到程序退出才释放
        //        NSString *imageName = [NSString stringWithFormat:@"%d", i+1];
        //        UIImage *image = [UIImage imageNamed:imageName];
        
        // imageNamed: 有内存缓存直到程序退出才释放(传入文件名)
        
        // UIImage *image = [UIImage imageNamed:filename];
        
        // imageWithContentsOfFile: 没有缓存,自动释放(传入文件的全路径)
        
//        NSBundle *bundle = [NSBundle mainBundle];
        
//        NSString *path = [bundle pathForResource:filename ofType:nil];
        
//        UIImage *image = [UIImage imageWithContentsOfFile:path];
        
        
        // 6.换另一个方法
        NSString *imageName = [NSString stringWithFormat:@"%d", i+1];
//        NSBundle *bundle = [NSBundle mainBundle];
//        NSString *path = [bundle pathForResource:imageName ofType:@"png"];
        NSString *path = [[NSBundle mainBundle] pathForResource:imageName ofType:@"jpg"];
//        self.imageView.image = [UIImage imageWithContentsOfFile:path];
        UIImage *image = [UIImage imageWithContentsOfFile:path];
        [imageArr addObject:image];
    }
    
    self.imageView.animationImages = imageArr;
    
    // 2.设置播放次数(1次)

    self.imageView.animationRepeatCount = 0;
    
    // 3.设置播放时间
//    self.imageView.animationDuration = 1.f;
    
    [self.imageView startAnimating];
    
    
//    self.imageView.animationDuration = 1.0;
//    CGFloat delay = self.imageView.animationDuration;
    
    // 4.释放内存
    // 调用animationImages的setter方法，并赋值为空，设置延迟时间
    [self.imageView performSelector:@selector(setAnimationImages:) withObject:nil afterDelay:self.imageView.animationDuration];
    
}

```
