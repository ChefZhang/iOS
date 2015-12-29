# 4.pragma mark指令

## 本节知识点:

* 【了解】#pragma mark指令的使用
***
1.#pragma mark指令的使用

* 功能:简单来说就是对代码的分组,方便代码查找和导航用的 它们告诉Xcode编译器,要在编辑器窗格顶部的方法和函数弹出菜单中将代码分隔开。一些类(尤其是一些控制器类)可能很长,方法和函数弹出菜单可以便于代码导航。此时加入#pragma 指令(#pragma是一个编译指令)对代码进行逻辑组织很有效果。

* 一个类里我们总会有一些方法的功能与性质是相差不多的,你可能会有把方法们分组的想法。Xcode已经有了类似的支持,它就是 #pragma mark。
    * 分组: #pragma mark 分组(标识)名称 
    ![分组.png](http://upload-images.jianshu.io/upload_images/328309-418589b5856d32ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    * 分隔线: #pragma mark - 
    ![分割线.png](http://upload-images.jianshu.io/upload_images/328309-a696da406fe0ed15.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
    * 分割线加分组: #pragma mark - 分组(标识)名称 
    ![分割线加分组.png](http://upload-images.jianshu.io/upload_images/328309-dae0208fb22d3609.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)