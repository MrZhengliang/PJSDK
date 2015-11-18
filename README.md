#泡椒网游戏联运SDK 

问题反馈：<pengjianbo@paojiao.cn>
#搭建
1、拷贝PJSDK-Final-xxx.jar到你的工程libs目录下



```xml
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE" />
<uses-permission android:name="android.permission.INTERNET"/>
<!--在SDCard中创建与删除文件权限  -->
<uses-permission android:name="android.permission.MOUNT_UNMOUNT_FILESYSTEMS"/>
<!-- 往SDCard写入数据权限 -->
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<!-- 从SDCard读取数据权限 -->
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW"/>
<uses-permission android:name="android.permission.SYSTEM_OVERLAY_WINDOW" />
<uses-permission android:name="android.permission.READ_PHONE_STATE"/>
```
4、配置Acitivity和Service
 
#使用
1、初始化

```java
PJSDK.initialize(getBaseContext(), APP_ID, APP_KEY, true);
```
2、登录注册

```java
PJSDK.doLogin(new LoginListener() {
```

3、支付

```java
// 订单标题，如：购买100元宝
```
4、FloatView控制

```java
PJSDK.showFloatingView();//显示悬浮LOGO
```
 5、提交玩家信息
 
 ```java
 RoleInfo roleInfo = new RoleInfo("胡哥哥", 69, "才高八斗", 7554);
 ```
 
#SDK升级
 PJSDK这个版本全新的代码，请把SDK 3.1以前的资源全部移除再使用
#混淆
```properties
#########################通用混淆配置，项目中有就不需要配置#####################
``` 
#常见问题及意见
1、屏幕旋转对话消失问题