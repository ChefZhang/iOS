# UIImageView

* UIImageView极其常用，功能比较专一：显示图片
 
    * @property(nonatomic,retain) UIImage *image; 
显示的图片

    * @property(nonatomic,copy) NSArray *animationImages; 
显示的动画图片

    * @property(nonatomic) NSTimeInterval animationDuration; 
动画图片的持续时间

    * @property(nonatomic) NSInteger      animationRepeatCount; 
动画的播放次数（默认是0，代表无限播放）

* UIImageView继承自UIImage，其中有一个属性contentMode，是指图片显示的样式


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

* 让图片具有毛玻璃昂效果

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


UIImageView的常见方法
* \- (void)startAnimating; // 开始动画
* \- (void)stopAnimating; // 停止动画
* \- (BOOL)isAnimating; // 是否正在执行动画