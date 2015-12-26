# UIImageView

* UIKit框架提供了非常多的UI控件，但并不是每一个都很常用，有些控件可能1年内都用不上，有些控件天天用，比如UIButton、UILabel、UIImageView、UITableView等等
* UIImageView极其常用，功能比较专一：显示图片
 
* @property(nonatomic,retain) UIImage *image; 
显示的图片

* @property(nonatomic,copy) NSArray *animationImages; 
显示的动画图片

* @property(nonatomic) NSTimeInterval animationDuration; 
动画图片的持续时间

* @property(nonatomic) NSInteger      animationRepeatCount; 
动画的播放次数（默认是0，代表无限播放）