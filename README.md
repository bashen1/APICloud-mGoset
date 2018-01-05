# APICloud-mGoset

<div class="outline">

[showSet](#a0)

[showOtherIOS](#a1)

[showOtherAndroid](#a2)

[isPush](#a3)

</div>

# **概述**

此模块可以检测APP通知是否打开，可以定位系统设置项（使用前请仔细阅读模块文档说明）

<div id="a0"></div>

# **showSet**

打开当前应用的系统设置项
showSet()

## 示例代码

```js
var mGoset = api.require('mGoset');
mGoset.showSet();
```

## 可用性

iOS系统，Android系统
可提供的1.0.0及更高版本

<div id="a1"></div>

# **showOtherIOS**

通过字符串打开具体设置项
showOtherIOS({params})

## params

url:
-类型：字符串
-描述：ios的pref项，具体看以下事例
-可接受的值(列举了一部分)： 

> App-Prefs:root=General&path=About  //跳转至设置--通用--关于本机
App-Prefs:root=General&path=ACCESSIBILITY  //跳转至设置--通用--辅助功能
App-Prefs:root=AIRPLANE_MODE  //跳转至设置--飞行模式
App-Prefs:root=Bluetooth  //跳转至设置--蓝牙
App-Prefs:root=General&path=DATE_AND_TIME  //跳转至设置--通用--时间与日期
App-Prefs:root=FACETIME  //跳转至设置--FaceTime
App-Prefs:root=General   //跳转至设置--通用
App-Prefs:root=General&path=Keyboard   //跳转至设置--通用--键盘
App-Prefs:root=CASTLE   //跳转至设置--iCloud
App-Prefs:root=CASTLE&path=STORAGE_AND_BACKUP  //跳转至设置--iCloud--用量
App-Prefs:root=General&path=INTERNATIONAL  //跳转至设置--通用--语言与地区
App-Prefs:root=LOCATION_SERVICES  //跳转至设置--通用--语言与地区
App-Prefs:root=ACCOUNT_SETTINGS  //跳转至设置--邮件
App-Prefs:root=MUSIC   //跳转至设置--音乐
App-Prefs:root=NOTES  //跳转至设置--备忘录
App-Prefs:root=NOTIFICATIONS_ID   //跳转至设置--通知
App-Prefs:root=Phone   //跳转至设置--电话
App-Prefs:root=Photos   //跳转至设置--照片与相机
App-Prefs:root=General&path=ManagedConfigurationList  //跳转至设置--通用--描述文件
App-Prefs:root=General&path=Reset  //跳转至设置--通用--还原
App-Prefs:root=Sounds&path=Ringtone  //跳转至设置--声音--电话铃声
App-Prefs:root=Safari  //跳转至设置--Safari
App-Prefs:root=Sounds  //跳转至设置--声音
App-Prefs:root=General&path=SOFTWARE_UPDATE_LINK  //跳转至设置--通用--软件更新
App-Prefs:root=STORE  //跳转至设置--iTunes Store与App Store
App-Prefs:root=TWITTER  //跳转至设置--Twitter
App-Prefs:root=FACEBOOK  //跳转至设置--FaceBook
App-Prefs:root=VIDEO  //跳转至设置--视频
App-Prefs:root=Wallpaper  //跳转至设置--墙纸
App-Prefs:root=WIFI  //跳转至设置--Wi-Fi
App-Prefs:root=INTERNET_TETHERING  //跳转至设置--Wi-Fi

## 示例代码

```js
var mGoset = api.require('mGoset');
var param = {
    url : 'App-Prefs:root=WIFI'   //打开网络WI-FI设置
};
mGoset.showOtherIOS(param);
```

## 可用性

iOS系统
可提供的1.0.0及更高版本

<div id="a2"></div>

# **showOtherAndroid**

通过字符串打开具体设置项
showOtherAndroid({params})

## params

url:
-类型：字符串
-描述：Android下的设置页面
-可接受的值： 

> android.settings.ACCESSIBILITY_SETTINGS  // 跳转系统的辅助功能界面
android.settings.AIRPLANE_MODE_SETTINGS  // 飞行模式，无线网和网络设置界面
android.settings.APPLICATION_DEVELOPMENT_SETTINGS  // 跳转开发人员选项界面
android.settings.APPLICATION_SETTINGS   // 跳转应用程序列表界面
android.settings.MANAGE_ALL_APPLICATIONS_SETTINGS // 跳转到应用程序界面【所有的】
android.settings.MANAGE_APPLICATIONS_SETTINGS  // 跳转 应用程序列表界面【已安装的】
android.settings.BLUETOOTH_SETTINGS   // 跳转系统的蓝牙设置界面
android.settings.DATA_ROAMING_SETTINGS   // 跳转到移动网络设置界面
android.settings.DATE_SETTINGS   // 跳转日期时间设置界面
android.settings.DISPLAY_SETTINGS   // 跳转手机显示和亮度界面
android.settings.DREAM_SETTINGS 【API 18及以上】跳转互动屏保
android.settings.INPUT_METHOD_SETTINGS   // 跳转语言和输入设备
android.settings.INTERNAL_STORAGE_SETTINGS // 跳转存储设置界面【内部存储】
android.settings.MEMORY_CARD_SETTINGS   // 跳转 存储设置 【记忆卡存储】
android.settings.LOCATION_SOURCE_SETTINGS   // 跳转位置服务界面
android.settings.NETWORK_OPERATOR_SETTINGS   // 跳转到 显示设置选择网络运营商。
android.settings.NFCSHARING_SETTINGS   // 显示NFC共享设置。 【API 14及以上】
android.settings.NFC_SETTINGS   // 显示NFC设置。这显示了用户界面,允许NFC打开或关闭。 【API 16及以上】
android.settings.PRIVACY_SETTINGS   // 跳转到备份和重置界面
android.settings.QUICK_LAUNCH_SETTINGS   // 跳转快速启动设置界面
android.settings.SECURITY_SETTINGS   // 跳转到安全设置界面
android.settings.SETTINGS   // 跳转到设置界面
android.settings.SOUND_SETTINGS // 跳转到声音设置界面
android.settings.SYNC_SETTINGS   // 跳转账户同步界面
android.settings.USER_DICTIONARY_SETTINGS   // 跳转用户字典界面
android.settings.WIFI_IP_SETTINGS   // 跳转至IP设定界面
android.settings.WIFI_SETTINGS   // 跳转Wifi列表设置

## 示例代码

```js
var mGoset = api.require('mGoset');
var param = {
    url : 'android.settings.WIFI_IP_SETTINGS'   //打开网络WI-FI设置
};
mGoset.showOtherAndroid(param);
```

## 可用性

Android系统
可提供的1.0.0及更高版本

<div id="a3"></div>

# **isPush**

查询当前应用是否开启通知，**Android只支持5及以上**
isPush(function(ret,err){})

## callback(ret, err)

ret：

- 类型：JSON对象
- 内部字段：

```js
{
    code :"1",              //状态码，字符串。0：推送关闭，1：推送打开
    msg:"推送打开"           //字符串
}
```

## 示例代码

```js
var mGoset = api.require('mGoset');
mGoset.isPush(function(ret,err){
    alert(JSON.stringify(ret));
});
```

## 可用性

iOS系统，Android系统
可提供的1.0.0及更高版本

