## 目录结构
- [对style和attr的引用](#1.0.0)
- [如何自定义属性](#2.0.0)
- [如何使用平台自带的属性](#3.0.0)
- [如何继承style](#4.0.0)
- ["Android："前出现‘@’和‘？’的区别](#5.0.0)
<h4 id="1.0.0"> 一.对style和attr的引用</h4>

1. 当引用平台的style做为style的parent时，“@android:style/主题”  == “@android:主题” == “android:style/主题 ” == “android:主题”;

2. 当引用平台的style作为属性的引用时，“@android:style/主题”；

3. 当引用自定义style作为其他style的parent时，“@style/主题” == “style/主题” == “主题”;

4. 当引用自定义style作为其他属性的引用时，“@style/主题”；

5. 当引用平台属性作为属性的引用时，“?android:attr/属性” == “?android:属性”;

6. 当引用自定义属性时，“?attr/属性” == “?属性”；

7. 上述六个情况中，可以在'@'或'？'后加入'*'以引用被隐藏（即平台私有）的资源；

8. 如果引用平台资源或属性时，可以将“Android:”放在斜杠“/”的后面，即，@android:style/主题”== @style/android:主题”,“?android:attr/属性”== “?attr/android:属性”；

<h4 id="1.0.0"> 二.如何自定义属性</h4>

1：  

     <resources>
        <attr name="anr">
            <enum name="none" value="0" />
            <enum name="thumbnail" value="1" />
            <enum name="drop" value="2" />
        </attr>
    </resources>

这种方式定义属性后，其他的<declare-styleable>块内可以直接使用，但不能带有任何名字或格式说明，e.g：

   

     <declare-styleable name="TextView">
          <attr name="anr">

     </declare-styleable>


下面是错误的：


     <declare-styleable name="TextView">
          <attr name="anr"  format="string">

    </declare-styleable>


因为这相当于重新定义了"anr"，这是不允许的。因此，<declare-styleable>块外出现的属性优先于<declare-styleable>块内出现的属性，即，如果<declare-styleable>块内出现某一带有format描述的属性，而<declare-styleable>块外也有一个同名属性（没有format说明），则是错误的。


此外，如果对首次出现在<declare-styleable>内的属性指定了format，则其他的<declare-styleable>内可直接使用这个属性，但不能再指定其他format。这种情况类似于使用首次出现<declare-styleable>块外的属性。


因此，在<declare-styleable>块外的属性最好都指明format说明，以便为<declare-styleable>块内使用。


e.g:


如果，


   <resources>
        <attr name="anr" />

   </resources>


然后，


   <declare-styleable name="TextView">
          <attr name="anr" format="dimension">

    </declare-styleable>


或者


    <declare-styleable name="TextView">
          <attr name="anr">
            <enum name="none" value="0" />
            <enum name="thumbnail" value="1" />
            <enum name="drop" value="2" />
         </attr>

    </declare-styleable>


这些都是错误的！

2:

    <declare-styleable name="Theme">
      <attr name="colorText"  format="color|reference"/>
      <attr name="colorForeground" format="color"/>
      <attr name="colorForegroundInverse" format="color"/>
    </declare-styleable>

这种方式定义属性的前提是此前没有对colorText， colorForeground，colorForegroundInverse的任何定义。同第一种一样，以后的<declare-styleable>块内可以直接使用，但不能再做其他改动，e.g:

    <declare-styleable name="TextView">
          <attr name="colorText">
    </declare-styleable>

或者：

    <declare-styleable name="TextView">
          <attr name="colorText">
          <attr name="colorForeground">
    </declare-styleable>

但下面是错误的：

    <declare-styleable name="TextView">
          <!--不能再有format="color|reference"说明-->
          <attr name="colorText" format="color|reference">
          <attr name="colorForeground">
    </declare-styleable>


<h4 id="1.0.0"> 三.如何使用平台自带的属性</h4>

    <declare-styleable name="FragmentArguments">
        <!--不能有格式说明-->
        <attr name="android:label" />
    </declare-styleable>

此时，在R.styleable内部会有个属性的定义,名为FragmentArguments_android_label。

但是，不能对平台自带的属性重新定义，e.g:

    <resources>
        <attr name="android:label" />
    </resources>

但可以这样：

     <resources>
        <attr name="label" format="string"/>
    </resources>

<h4 id="1.0.0"> 四.如何继承style</h4>

可以使用点‘.’和“parent”来继承自定义的style，而要想继承平台style，则只能使用“parent”。


e.g:


   1.
    <style name="HelloTheme" parent="@android:style/Theme.Light" >
          <item name="colorForeground">#770000</item>
          <item name="colorBackground">#000000</item>
          <item name="colorText">#00ff00</item>
          <item name="android:windowBackground" >@drawable/windowoverlay </item>
          <item name="android:windowNoTitle">false</item>

    </style>


   2.
     <style name="HelloTheme"  parent="HelloTheme.MyHelloTheme">
        <item name="windowBackground" >@drawable/overlaybk </item>
        <item name="colorText">#00ff00</item>
    </style>
    <style name="HelloTheme.Hello" >
        <!--<item name="android:background">?attr/windowBackground</item>-->
        <!--<item name="android:textColor">?attr/colorText</item>-->
        <item name="android:background">?windowBackground</item>
        <item name="android:textColor">?colorText</item>

    </style>


   3.
   <style name="Holo">
        <item name="textViewStyle">@style/HelloTheme.Hello</item>

    </style>


   4.
   <style name="Holo.TextViewStyle" />

如果对一个TextView使用Holo.TextViewStyle时，不会起到任何作用。应该直接使用：

   <style name="TextViewStyle">
        <item name="android:background">?windowBackground</item>
        <item name="android:textColor">?colorText</item>
   </style>

或者

   <style name="TextViewStyle_1"  parent="TextViewStyle" >
   
或者
 
   <style name="TextViewStyle.TextViewStyle_1">

由此可知，属性引用（reference）可以传递，当然前提是应用或活动的主题（theme）中使用了windowBackground和colorText，上例中：

    <item name="android:background">?windowBackground</item>
     <item name="android:textColor">?colorText</item>

等价于：

    <item name="android:background">@drawable/overlaybk</item>
     <item name="android:textColor">#00ff00</item>

因为，windowBackground和colorText作为两个属性的引用，在这里已被设置：

    <style name="HelloTheme"  parent="HelloTheme.MyHelloTheme">
        <item name="windowBackground" >@drawable/overlaybk </item>
        <item name="colorText">#00ff00</item>
    </style>
   
自定义属性时，在parent处指定的继承平台已有属性时偶尔会提示资源不存在

e.g:


    parent="@android:style/TextAppearance.Holo.Light.Inverse"

    error: Error retrieving parent for item: No resource found that matches the given name '@android:style/TextAppearance.Holo.Light.Inverser'.


这种写法是错误的，虽然平台下的data/res/styles.xml内有该属性的定义，但是平台的android.R.style类内并不存在TextAppearance_Holo_Light_Inverse，因为此类属性是平台的私有属性，不公开的。所以，也不能使用android.R.style.TextAppearance_Holo_Light_Inverse.


若要避免错误，可以这样书写：parent="@*android:style/TextAppearance.Holo.Light.Inverse" ,或去掉'@'和(或)'style/'。


最后，如果style的名字内既出现了点‘.’，也使用“parent”，则该style只继承了parent指向的style，style的 "name"里的‘.’不会起作用。如果在style的"name"内出现了‘.’，而又没有使用"parent"，则name里的点'.'之前的名字必须存在定义。而如果使用了parent，name内点'.'之前的任何名字可以不存在定义。


<h4 id="1.0.0"> 五."Android："前出现‘@’和‘？’的区别</h4>

在定义style时经常会遇到此类情况，例如：


 <style name="Theme.IconMenu" parent="Theme.Holo">
        <!-- Menu/item attributes -->
        <item name="android:itemTextAppearance">@android:style/TextAppearance.Widget.IconMenu.Item</item>
        <item name="android:itemBackground">?android:attr/selectableItemBackground</item>
        <item name="android:itemIconDisabledAlpha">?android:attr/disabledAlpha</item>
        <item name="android:horizontalDivider">@android:drawable/divider_horizontal_dark</item>
        <item name="android:verticalDivider">@android:drawable/divider_vertical_dark</item>
        <item name="android:windowAnimationStyle">@android:style/Animation.OptionsPanel</item>
        <item name="android:moreIcon">@android:drawable/ic_menu_more</item>
        <item name="android:background">@null</item>
    </style>


其中，<item name="android:itemTextAppearance">@android:style/TextAppearance.Widget.IconMenu.Item</item>表明"android:itemTextAppearance"为一个style类型，它引用了平台的另一个style（TextAppearance.Widget.IconMenu.Item）。而 <item name="android:itemIconDisabledAlpha">?android:attr/disabledAlpha</item>则表明"android:itemIconDisabledAlpha"的属性值引用当前主题下的disabledAlpha。


