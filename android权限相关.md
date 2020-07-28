[为什么说在Android中请求权限从来都不是一件简单的事情？](https://mp.weixin.qq.com/s?__biz=MzA5MzI3NjE2MA==&mid=2650251007&idx=1&sn=f8961f1f2d778190ae42b71d3a43685b&chksm=88636f90bf14e686317c725c55ea860a71296593890bf8a162d1e2b7305233db7ff285f03cd1&mpshare=1&scene=23&srcid=0728Au7k5rdUSxWIpnTXj43g&sharer_sharetime=1595897198747&sharer_shareid=90faf7dc0a3f3a045a59c3239c0185f4#rd)











android.permission.EXPAND_STATUS_BAR允许一个程序扩展收缩在状态栏,android开发网提示应该是一个类似Windows Mobile中的托盘程序

android.permission.FACTORY_TEST作为一个工厂测试程序，运行在root用户

android.permission.FLASHLIGHT访问闪光灯,android开发网提示HTC Dream不包含闪光灯

android.permission.FORCE_BACK允许程序强行一个后退操作是否在顶层activities

android.permission.FOTA_UPDATE暂时不了解这是做什么使用的，android开发网分析可能是一个预留权限.

android.permission.GET_ACCOUNTS访问一个帐户列表在Accounts Service中

android.permission.GET_PACKAGE_SIZE允许一个程序获取任何package占用空间容量

android.permission.GET_TASKS允许一个程序获取信息有关当前或最近运行的任务，一个缩略的任务状态，是否活动等等

android.permission.HARDWARE_TEST允许访问硬件

android.permission.INJECT_EVENTS允许一个程序截获用户事件如按键、触摸、轨迹球等等到一个时间流，android开发网提醒算是hook技术吧

android.permission.INSTALL_PACKAGES允许一个程序安装packages

android.permission.INTERNAL_SYSTEM_WINDOW允许打开窗口使用系统用户界面

android.permission.ACCESS_CHECKIN_PROPERTIES允许读写访问“properties”表在checkin数据库中，改值可以修改上传。

android.permission.ACCESS_COARSE_LOCATION允许一个程序访问CellID或WiFi热点来获取粗略的位置

android.permission.ACCESS_FINE_LOCATION允许一个程序访问精良位置(如GPS)

android.permission.WRITE_CONTACTS允许程序写入但不读取用户联系人数据

android.permission.WRITE_GSERVICES允许程序修改Google服务地图

android.permission.WRITE_OWNER_DATA允许一个程序写入但不读取所有者数据

android.permission.WRITE_SETTINGS允许程序读取或写入系统设置

android.permission.WRITE_SMS允许程序写短信

android.permission.WRITE_SYNC_SETTINGS允许程序写入同步设置

android.permission.ACCESS_LOCATION_EXTRA_COMMANDS允许应用程序访问额外的位置提供命令

android.permission.ACCESS_MOCK_LOCATION允许程序创建模拟位置提供用于测试

android.permission.ACCESS_NETWORK_STATE允许程序访问有关GSM网络信息

android.permission.ACCESS_SURFACE_FLINGER允许程序使用SurfaceFlinger底层特性

android.permission.ACCESS_WIFI_STATE允许程序访问Wi-Fi网络状态信息

android.permission.ADD_SYSTEM_SERVICE允许程序发布系统级服务

android.permission.BATTERY_STATS允许程序更新手机电池统计信息

android.permission.BLUETOOTH允许程序连接到已配对的蓝牙设备

android.permission.BLUETOOTH_ADMIN允许程序发现和配对蓝牙设备

android.permission.BROADCAST_PACKAGE_REMOVED允许程序广播一个提示消息在一个应用程序包已经移除后

android.permission.BROADCAST_STICKY允许一个程序广播常用intents

android.permission.CALL_PHONE允许一个程序初始化一个电话拨号不需通过拨号用户界面需要用户确认

android.permission.DELETE_CACHE_FILES允许程序删除缓存文件

android.permission.DELETE_PACKAGES允许一个程序删除包

android.permission.DEVICE_POWER允许访问底层电源管理

android.permission.DIAGNOSTIC允许程序RW诊断资源

android.permission.DISABLE_KEYGUARD允许程序禁用键盘锁

android.permission.DUMP允许程序返回状态抓取信息从系统服务

android.permission.CALL_PRIVILEGED允许一个程序拨打任何号码，包含紧急号码无需通过拨号用户界面需要用户确认

android.permission.CAMERA请求访问使用照相设备

android.permission.CHANGE_COMPONENT_ENABLED_STATE允许一个程序是否改变一个组件或其他的启用或禁用

android.permission.CHANGE_CONFIGURATION允许一个程序修改当前设置，如本地化

android.permission.CHANGE_NETWORK_STATE允许程序改变网络连接状态

android.permission.CHANGE_WIFI_STATE允许程序改变Wi-Fi连接状态

android.permission.CLEAR_APP_CACHE允许一个程序清楚缓存从所有安装的程序在设备中

android.permission.CLEAR_APP_USER_DATA允许一个程序清除用户设置

android.permission.CONTROL_LOCATION_UPDATES允许启用禁止位置更新提示从无线模块

android.permission.REBOOT请求能够重新启动设备

android.permission.RECEIVE_BOOT_COMPLETED允许一个程序接收到ACTION_BOOT_COMPLETED广播在系统完成启动

android.permission.RECEIVE_MMS允许一个程序监控将收到MMS彩信,记录或处理

android.permission.RECEIVE_SMS允许程序监控一个将收到短信息，记录或处理

android.permission.RECEIVE_WAP_PUSH允许程序监控将收到WAP PUSH信息

android.permission.RECORD_AUDIO允许程序录制音频

android.permission.REORDER_TASKS允许程序改变Z轴排列任务

android.permission.RESTART_PACKAGES允许程序重新启动其他程序

android.permission.SEND_SMS允许程序发送SMS短信

android.permission.INTERNET允许程序打开网络套接字

android.permission.MANAGE_APP_TOKENS允许程序管理(创建、催后、 z-order默认向z轴推移)程序引用在窗口管理器中

android.permission.MASTER_CLEAR目前还没有明确的解释，android开发网分析可能是清除一切数据，类似硬格机

android.permission.MODIFY_AUDIO_SETTINGS允许程序修改全局音频设置

android.permission.MODIFY_PHONE_STATE允许修改话机状态，如电源，人机接口等

android.permission.MOUNT_UNMOUNT_FILESYSTEMS允许挂载和反挂载文件系统可移动存储

android.permission.PERSISTENT_ACTIVITY允许一个程序设置他的activities显示

android.permission.PROCESS_OUTGOING_CALLS允许程序监视、修改有关播出电话

android.permission.READ_CALENDAR允许程序读取用户日历数据

android.permission.READ_CONTACTS允许程序读取用户联系人数据

android.permission.READ_FRAME_BUFFER允许程序屏幕波或和更多常规的访问帧缓冲数据

android.permission.READ_INPUT_STATE允许程序返回当前按键状态

android.permission.READ_LOGS允许程序读取底层系统日志文件

android.permission.READ_OWNER_DATA允许程序读取所有者数据

android.permission.READ_SMS允许程序读取短信息

android.permission.READ_SYNC_SETTINGS允许程序读取同步设置

android.permission.READ_SYNC_STATS允许程序读取同步状态

android.permission.SET_ACTIVITY_WATCHER允许程序监控或控制activities已经启动全局系统中

android.permission.SET_ALWAYS_FINISH允许程序控制是否活动间接完成在处于后台时

android.permission.SET_ANIMATION_SCALE修改全局信息比例

android.permission.SET_DEBUG_APP配置一个程序用于调试

android.permission.SET_ORIENTATION允许底层访问设置屏幕方向和实际旋转

android.permission.SET_PREFERRED_APPLICATIONS允许一个程序修改列表参数PackageManager.addPackageToPreferred()和PackageManager.removePackageFromPreferred()方法

android.permission.SET_PROCESS_FOREGROUND允许程序当前运行程序强行到前台

android.permission.SET_PROCESS_LIMIT允许设置最大的运行进程数量

android.permission.SET_TIME_ZONE允许程序设置时间区域

android.permission.SET_WALLPAPER允许程序设置壁纸

android.permission.SET_WALLPAPER_HINTS允许程序设置壁纸hits

android.permission.SIGNAL_PERSISTENT_PROCESSES允许程序请求发送信号到所有显示的进程中

android.permission.STATUS_BAR允许程序打开、关闭或禁用状态栏及图标Allows an application toopen, close, or disable the status bar and its icons.

android.permission.SUBSCRIBED_FEEDS_READ允许一个程序访问订阅RSS Feed内容提供

android.permission.SUBSCRIBED_FEEDS_WRITE系统暂时保留改设置,android开发网认为未来版本会加入该功能。

android.permission.SYSTEM_ALERT_WINDOW允许一个程序打开窗口使用TYPE_SYSTEM_ALERT，显示在其他所有程序的顶层

android.permission.VIBRATE允许访问振动设备

android.permission.WAKE_LOCK允许使用PowerManager的 WakeLocks保持进程在休眠时从屏幕消失

android.permission.WRITE_APN_SETTINGS允许程序写入API设置

android.permission.WRITE_CALENDAR允许一个程序写入但不读取用户日历数据

可以看出Android中对资源以及服务的访问都非常严格，另外，在程序打包成APK的时候也需要对软件进行签名。

获取精确位置    android.permission.ACCESS_FINE_LOCATION，通过GPS芯片接收卫星的定位信息，定位精度达10米以内    

访问定位额外命令    android.permission.ACCESS_LOCATION_EXTRA_COMMANDS，允许程序访问额外的定位提供者指令    

获取模拟定位信息    android.permission.ACCESS_MOCK_LOCATION，获取模拟定位信息，一般用于帮助开发者调试应用    

获取网络状态    android.permission.ACCESS_NETWORK_STATE，获取网络信息状态，如当前的网络连接是否有效    

访问Surface Flinger    android.permission.ACCESS_SURFACE_FLINGER，Android平台上底层的图形显示支持，一般用于游戏或照相机预览界面和底层模式的屏幕截图    

获取WiFi状态    android.permission.ACCESS_WIFI_STATE，获取当前WiFi接入的状态以及WLAN热点的信息    

账户管理    android.permission.ACCOUNT_MANAGER，获取账户验证信息，主要为GMail账户信息，只有系统级进程才能访问的权限    

验证账户    android.permission.AUTHENTICATE_ACCOUNTS，允许一个程序通过账户验证方式访问账户管理ACCOUNT_MANAGER相关信息    

电量统计    android.permission.BATTERY_STATS，获取电池电量统计信息    

绑定小插件    android.permission.BIND_APPWIDGET，允许一个程序告诉appWidget服务需要访问小插件的数据库，只有非常少的应用才用到此权限    

绑定设备管理    android.permission.BIND_DEVICE_ADMIN，请求系统管理员接收者receiver，只有系统才能使用    

绑定输入法    android.permission.BIND_INPUT_METHOD，请求InputMethodService服务，只有系统才能使用    

绑定RemoteView    android.permission.BIND_REMOTEVIEWS，必须通过RemoteViewsService服务来请求，只有系统才能用    

绑定壁纸    android.permission.BIND_WALLPAPER，必须通过WallpaperService服务来请求，只有系统才能用    

使用蓝牙    android.permission.BLUETOOTH，允许程序连接配对过的蓝牙设备    

蓝牙管理    android.permission.BLUETOOTH_ADMIN，允许程序进行发现和配对新的蓝牙设备    

变成砖头    android.permission.BRICK，能够禁用手机，非常危险，顾名思义就是让手机变成砖头    

应用删除时广播    android.permission.BROADCAST_PACKAGE_REMOVED，当一个应用在删除时触发一个广播    

收到短信时广播    android.permission.BROADCAST_SMS，当收到短信时触发一个广播    

连续广播    android.permission.BROADCAST_STICKY，允许一个程序收到广播后快速收到下一个广播    

WAP PUSH广播    android.permission.BROADCAST_WAP_PUSH，WAPPUSH服务收到后触发一个广播    

拨打电话    android.permission.CALL_PHONE，允许程序从非系统拨号器里输入电话号码    

通话权限    android.permission.CALL_PRIVILEGED，允许程序拨打电话，替换系统的拨号器界面    

拍照权限    android.permission.CAMERA，允许访问摄像头进行拍照    

改变组件状态    android.permission.CHANGE_COMPONENT_ENABLED_STATE，改变组件是否启用状态    

改变配置    android.permission.CHANGE_CONFIGURATION，允许当前应用改变配置，如定位    

改变网络状态    android.permission.CHANGE_NETWORK_STATE，改变网络状态如是否能联网    

改变WiFi多播状态    android.permission.CHANGE_WIFI_MULTICAST_STATE，改变WiFi多播状态    

改变WiFi状态    android.permission.CHANGE_WIFI_STATE，改变WiFi状态    

清除应用缓存    android.permission.CLEAR_APP_CACHE，清除应用缓存    

清除用户数据    android.permission.CLEAR_APP_USER_DATA，清除应用的用户数据    

底层访问权限    android.permission.CWJ_GROUP，允许CWJ账户组访问底层信息    

手机优化大师扩展权限    android.permission.CELL_PHONE_MASTER_EX，手机优化大师扩展权限    

控制定位更新    android.permission.CONTROL_LOCATION_UPDATES，允许获得移动网络定位信息改变    

删除缓存文件    android.permission.DELETE_CACHE_FILES，允许应用删除缓存文件    

删除应用    android.permission.DELETE_PACKAGES，允许程序删除应用    

电源管理    android.permission.DEVICE_POWER，允许访问底层电源管理    

应用诊断    android.permission.DIAGNOSTIC，允许程序到RW到诊断资源    

禁用键盘锁    android.permission.DISABLE_KEYGUARD，允许程序禁用键盘锁    

转存系统信息    android.permission.DUMP，允许程序获取系统dump信息从系统服务    

状态栏控制    android.permission.EXPAND_STATUS_BAR，允许程序扩展或收缩状态栏    

工厂测试模式    android.permission.FACTORY_TEST，允许程序运行工厂测试模式    

使用闪光灯    android.permission.FLASHLIGHT，允许访问闪光灯    

强制后退    android.permission.FORCE_BACK，允许程序强制使用back后退按键，无论Activity是否在顶层    

访问账户Gmail列表    android.permission.GET_ACCOUNTS，访问GMail账户列表    

获取应用大小    android.permission.GET_PACKAGE_SIZE，获取应用的文件大小    

获取任务信息    android.permission.GET_TASKS，允许程序获取当前或最近运行的应用    

允许全局搜索    android.permission.GLOBAL_SEARCH，允许程序使用全局搜索功能    

硬件测试    android.permission.HARDWARE_TEST，访问硬件辅助设备，用于硬件测试    

注射事件    android.permission.INJECT_EVENTS，允许访问本程序的底层事件，获取按键、轨迹球的事件流    

安装定位提供    android.permission.INSTALL_LOCATION_PROVIDER，安装定位提供    

安装应用程序    android.permission.INSTALL_PACKAGES，允许程序安装应用    

内部系统窗口    android.permission.INTERNAL_SYSTEM_WINDOW，允许程序打开内部窗口，不对第三方应用程序开放此权限    

访问网络    android.permission.INTERNET，访问网络连接，可能产生GPRS流量    

结束后台进程    android.permission.KILL_BACKGROUND_PROCESSES，允许程序调用killBackgroundProcesses(String).方法结束后台进程    

管理账户    android.permission.MANAGE_ACCOUNTS，允许程序管理AccountManager中的账户列表    
