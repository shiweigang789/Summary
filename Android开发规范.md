# 1  命名规范

## 1.1  Class命名
 
- 任何类名都应该使用 UpperCamelCase （驼峰法）命名, 例如:

  AndroidActivity, NetworkHelper, UserFragment, PerActivity
  
- 不能以下划线或美元符号开始，也不能以下划线或美元符号结束
- 严禁使用拼音与英文混合的方式
- 除了常见的英文缩写，尽量避免缩写
  
## 1.2  变量名

- 变量名：静态常量使用大写字母，使用下划线“_”分词。
  ```
  public static String A_ROUTER_GUIDE_ACTIVITY = ""
  ```
- 非静态成员变量、局部变量、首字母小写，驼峰式分词。
  ```
  private int scrollDistance
  ```
- Activity、Fragment、Adapter、View 的子类的成员变量：驼峰式分词。
  ```
  public class NewWalletHomeFragmentVm extends BaseFragmentRvVM{}
  ```
- 方法名：首字母小写，驼峰式分词。
  ```
  public void setCurrentClickNewWalletHomePageTokenListVm(){}
  ```

## 1.3 资源文件命名

- layout 文件的命名方式 如下：
  ```
  Activity 的 layout 以 activity_ 开头 
  Fragment 的 layout 以 fragment_ 开头 
  Dialog 的 layout 以 dialog_ 开头 
  include 的 layout 以 include_ 开头 
  ListView 的行 layout 以 list_item_ 开头 
  RecyclerView 的 item layout 以 recycle_item_ 开头 
  GridView 的行 layout 以 grid_item_ 开头
  ```
- drawable 资源名称以小写单词+下划线的方式命名 业务功能描述_控件描述_控件状态限定词  如下：

  类型    |	前缀	    |例如   |
  |----- |---- |---- |
  |Selector	|selector_	|selector_button_cancel|
  |Background	|bg_	|bg_rounded_button|
  |Circle	|circle_	|circle_white|
  |Progress	|progress_	|progress_circle_purple|
  |Divider	|divider_	|divider_grey|

 - 图片以ic_为前缀，与功能、状态一起命名  如下：

   ic_accept_normal,ic_accept_pressed

 - anim 资源名称以小写单词+下划线的方式命名  如下：

   anim_fade_out, anim_push_down_in 

 - color资源命名，色值均使用大写
   ```
   <color name="color_33B5E5E5">#33B5E5E5</color> 
   ```
 - dimen资源直接使用数值命名  如下：
   ```
   <dimen name="dimen_4dp">4dp</dimen>， <dimen name="text_size_34sp">34sp</dimen>
   ```
     
- 控件id命名  如下：

  控件   |	 缩写|  控件 | 缩写  |
  |-----|----- |-----  |-----  |
  |TextView|tv|ImageButton|ib|
  |EditText|et|CheckBox|cb|
  |WebView|wv|RadioButton|rb|
  |ImageView|iv|SeekBar|sb|
  |VideoView|vv|ProgressBar|pb|
  |MediaController|mc|Spinner|spr|
  |ListView|lv|SerachView|sev|
  |GridView|gv|Button|btn|Gallery|gly|
  |TimePicker|tp|LinearLayout|ll|
  |DatePicker|dp|RelativeLayout|rl|
  |ScrollView|sv|FrameLayout|fl|
  |RecyclerView|rv|

## 1.4 路由路径命名

 - 路径命名统一放在ConstantsARouteService类中
 - 命名规则则为A_ROUTER_model名称_当前类名
 - 路径规则为/model名称/当前类名
 - 在命名属性上加入注释（当前路径的界面信息，需要传递的参数，参数的类型，参数可能的值及其含义） 如下
      ```
      /**
      * 密码登录界面和密码设置界面
      *
      * @param type int // 密码输入类型 1为密码登录 2为密码设置 0为二次验证
      */
     String A_ROUTER_IDENTIFICATION_PIN_ACTIVITY = "/login/IdentificationPinActivity";
     ```

# 2 代码规范

## 2.1 语法规范

- 类中一些无用的代码、无用变量、无用的import和注释的代码及时清除
- 数据实体类中禁止处理计算等相应逻辑,重写toString方法利于打印日志
- 一个函数方法的长度不要超过80行（把能抽取出来单独封装的代码抽取出来）
- 计算量耗时的操作或者IO操作要开启子线程，防止ANR异常
- 一行代码的长度：不要超过160个字符。
- 一个方法的长度：不要超过：80行。
- 一个方法的参数列表不要超过：7个。
- if 嵌套层次：不要超过4层。（多用return）
- 不能保证一个对象不为空的情况下，一定要做判空处理
  ```
  if(user != null){}
  if(user == null) return;
  ```
- 捕获的异常要做相应的处理或者打印日志
  ```
  try {
        getObjectMapper().writeValueAsString(identityKeystore)
    } catch (e: JsonProcessingException) {
        e.printStackTrace()
        Logutils.eTag(TAG,e.message)
        return false
    }
- 比较字符是否相同时使用 示例：

  ```
  if(TextUtils.equal(a,b){
  }
  ```
  
- 禁止在循环体中多次创建对象引用 示例：

  ```
  Object obj = null;
  for (int i = 0; i <= count; i++)
  {
    obj = new Object();
  }
  ```
  
- 禁止”魔术数”：（所有常量使用常量定义其特定含义）

  ```
  switch(i) {
       case 1:
         mManager.updloadTag();
       break;
         mManager.uploadTabMore();
       case 2:
         // do something
       break;
        // ...
       case 3:
        // ....
       break;
     }
  ```
  
- 网络Api接口的方法名和Request请求种的方法名保持一致
   ```
   Api中
   @POST("app/check_update")
   fun checkUpdate(@Body requestBody: RequestBody): Observable<ApiResponse<UpdateInfo>>
   Request中
   fun checkUpdate(result: Response.Result<UpdateInfo>) {}
   ```

## 2.2 注释规范

- 新建的类，添加类信息 （创建人，日期，类作用的）
  ```
  /**
    *  作者    Owen
    *  时间    2019/9/23 14:16
    *  文件    HiWallet-andorid
    *  描述    创建Identity的帮助类
    */
  ```

- 数据实体类 标明每个属性的作用，可能的一些数值和数值代表的意义
  ```
  @Parcelize
  data class UpdateInfo(
          val description: String,  //最新版本描述
          val downloadUrl: String,  // 下载链接
          val hasUpdate: String,    // 是否有新版本（0、无；1、有)
          val isForcedUpdates: Int, // 是否强制更新
          val version: String       // 最新版本
  ) : Parcelable
  ```
- 函数方法注释要说明方法的作用，参数要说明意义及可能的值代表的意义
  ```
  /**
   * Base64对json数据进行加密
   * @param jsonByteArray json数据的字节数组
   */
  private fun encodeBase64(jsonByteArray: ByteArray): String {
      val bodyStr = String(Base64.encodeBase64(jsonByteArray))
      LogUtils.dTag(TAG, "bodyStr >>> $bodyStr")
      return bodyStr
  }
  ```

## 2.3 日志规范
    
- 需要了解数据变化的地方，一定要添加日志信息
- 网络日志TAG = "NET_当前类名"
- 钱包相关TAG = "WALLET_当前类名"
- 其他日志TGA = "当前类名"
- json数据使用LogUtils.json(TAG,json)
- 调试日志使用LogUtils.dTag(TAG,data)
- 异常日志使用LogUtils.eTag(TAG,json)  

# 3 资源释放

- 动态注册BroadCastReceiver时，registerReceiver() 和 unregisterReceiver()要成对出现
- 注册的EventBus事件在不使用时取消注册
- 读写文件的数据流及时关闭
- 打开的数据库在不使用时及时关闭

#### 根据项目要求持续更新...

参考资料[Android开发规范](https://github.com/shiweigang789/Summary/blob/master/Android%E5%BC%80%E5%8F%91%E8%A7%84%E8%8C%83.pdf)



