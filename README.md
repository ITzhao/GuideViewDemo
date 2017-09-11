# GuideViewDemo
GuideViewDemo是一款支持gif的引导页，高效封装，代码简洁
**你的星星，是我努力的最大的动力**

![Demo.gif](http://upload-images.jianshu.io/upload_images/3601550-e892f0c020e5e4ee.gif?imageMogr2/auto-orient/strip)

#### 简单实用：
```
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    self.window = [[UIWindow alloc]initWithFrame:[UIScreen mainScreen].bounds];
    self.window.backgroundColor = [UIColor whiteColor];
    [self.window makeKeyAndVisible];
    // if 条件 是 判断是否是第一次进入，如果是第一次 就就如引导页，不是就设置正常的根控制器
    if (YES) {
        GuideView *vc = [[GuideView alloc]init];
        [vc showGuideViewWithImageArray:@[@"10.gif",@"1.png",@"2.png",@"3.png"] WindowRootController:[ViewController new]];
        self.window.rootViewController = vc;
    }else{
      /**-------------------你工程的根控制器--------------**/
    }
    return YES;
}
```

