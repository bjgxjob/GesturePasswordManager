# GesturePasswordManager
手势密码的控件
用于应用内手势密码，保护应用内隐私
本控件以实现x秒之后无操作自动锁屏。使用时需要手势密码保护的activity实现ISecurityGesture.java接口.

需要手势密码保护的Activity实现ISecurityGesture.java这个接口标明需要锁屏。并且要重载Activity的Activity.onUserInteraction()的, 在这个方法里调用 GesturePasswordManager.userInteraction() 即可实现n秒后自动锁屏;
在使用本控件时，app初始化的时候调用使用密码控件时，在app初始化时调用GesturePasswordManager.getInstance().startWatch(getApplication());即可实现自动锁屏

