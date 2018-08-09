1. ase框架需要一个守护controller，标注@com.eas.android.actsoul.annotation.MainController，否则不会执行Operation等。
2. controller可以传入intent来区分起始步骤
3. 桌面作为一个特殊应用，他的stack是有特定的stack的，启动其他应用的时候都是会启动到其他的stack里面去，而这就会涉及到stack间动画处理,这个stack的切换动画会有特别
应用作为桌面的时候，需要设置显示壁纸，这样才不会显示出黑屏
修改方法有两种：
1：更改theme为系统的wallpaper类型（这个有可能会影响到显示）：  
比如说android:theme="@android:style/Theme.Wallpaper"  
或者是Theme.Wallpaper.NoTitleBar.Fullscreen这种衍生的，只要有wallpaper就OK  
2：在activity里面设置wallpaper window flag：  
getWindow().setFlags(WindowManager.LayoutParams.FLAG_SHOW_WALLPAPER, WindowManager.LayoutParams.FLAG_SHOW_WALLPAPER);  

4. 