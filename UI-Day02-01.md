# UILabel

### 什么是UILabel

 UILabel极其常用，功能单一，用于显示文字

### UILabel的常见属性
```objc
    显示的文字
    @property(nullable, nonatomic,copy)   NSString           *text;
    字体大小
    @property(null_resettable, nonatomic,strong) UIFont      *font;     
    字体颜色
    @property(null_resettable, nonatomic,strong) UIColor     *textColor;    
    文字的对齐方式
    @property(nonatomic)        NSTextAlignment    textAlignment;
    文字行数
    @property(nonatomic) NSInteger numberOfLines;
    换行模式
    @property(nonatomic)        NSLineBreakMode    lineBreakMode;
```

* 代码参考

```objc
    // 1.1 创建UILabel对象，并初始化frame
    UILabel *label = [[UILabel alloc] initWithFrame:CGRectMake(20, 20, 200, 120)];
    
    // 1.2 设置center
    label.center = self.view.center;
    
    // 1.3 设置背景颜色
    label.backgroundColor = [UIColor brownColor];
    
    // 1.4 设置文字
    label.text = @"这是一个彭彭和丁满的故事，非常非常的长,it is a long story!!! what do you think?";
    
    // 1.5 居中
    /*
     NSTextAlignmentLeft      = 0,    // Visually left aligned
     #if TARGET_OS_IPHONE
     NSTextAlignmentCenter    = 1,    // Visually centered
     NSTextAlignmentRight     = 2,    // Visually right aligned
     #else // !TARGET_OS_IPHONE
     NSTextAlignmentRight     = 1,    // Visually right aligned
     NSTextAlignmentCenter    = 2,    // Visually centered
     #endif
     NSTextAlignmentJustified = 3,    // Fully-justified. The last line in a paragraph is natural-aligned.
     NSTextAlignmentNatural   = 4,    // Indicates the default alignment for script
     */
    label.textAlignment = NSTextAlignmentCenter;
    
    // 1.6 设置字体大小
    label.font = [UIFont boldSystemFontOfSize:20.f];
    
    // 1.7 设置文字的颜色
    label.textColor = [UIColor magentaColor];
    
    // 1.8 设置阴影(默认是有值)
    label.shadowOffset = CGSizeMake(-3, 4);
    label.shadowColor = [UIColor whiteColor];
    
    // 1.9 设置行数(0:自动换行)，如果行数设置为0，那么显示模式就失去了设置的意义
    label.numberOfLines = 0;
    
    // 1.10 显示模式
    /*
    NSLineBreakByWordWrapping = 0,     	// Wrap at word boundaries, default
    NSLineBreakByCharWrapping,		// Wrap at character boundaries
    NSLineBreakByClipping,		// Simply clip
    NSLineBreakByTruncatingHead,	// Truncate at head of line: "...wxyz"
    NSLineBreakByTruncatingTail,	// Truncate at tail of line: "abcd..."
    NSLineBreakByTruncatingMiddle	// Truncate middle of line:  "ab...yz"
     */
    label.lineBreakMode = NSLineBreakByTruncatingMiddle;
    
    
    // 2.0 添加到控制器的view中
    [self.view addSubview:label];
```