#### -AppTheme 属性详解

    <style name="AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
        <!--Appbar背景色，应用的主要色调，actionBar默认使用该颜色-->
        <item name="android:colorPrimary">@color/material_animations_primary</item>
        <!--设置actionbar样式-->
        <item name="android:actionBarStyle">@style/ActionBarBaseStyle</item>
        <!--状态栏颜色，应用的主要暗色调，statusBarColor默认使用该颜色-->
        <item name="android:colorPrimaryDark">@color/material_animations_primary_dark</item>
        <!--状态栏颜色，默认使用colorPrimaryDark-->
        <item name="android:statusBarColor">@color/material_animations_primary_dark</item>
        <!--页面背景色-->
        <item name="android:windowBackground">@color/light_grey</item>
        <!--底部导航栏颜色-->
        <item name="android:navigationBarColor">@color/navigationColor</item>
        <!--应用的主要文字颜色，actionBar的标题文字默认使用该颜色-->
        <item name="android:textColorPrimary">@android:color/black</item>
        <!--ToolBar上的Title颜色-->
        <item name="android:textColorPrimaryInverse">@color/text_light</item>
        <!--应用的前景色，ListView的分割线，switch滑动区默认使用该颜色-->
        <item name="android:colorForeground">@color/colorForeground</item>
        <!--应用的背景色，popMenu的背景默认使用该颜色-->
        <item name="android:colorBackground">@color/colorForeground</item>
        <!--弹出菜单的样式-->
        <item name="android:popupMenuStyle">@style/ActionBarBaseStyle</item>
        <!--一般控件的选种效果默认采用该颜色-->
        <item name="android:colorAccent">@color/colorAccent</item>
        <!--控件选中时的颜色，默认使用colorAccent-->
        <item name="android:colorControlActivated">@color/colorControlActivated</item>
        <!--各个控制控件的默认颜色-->
        <item name="android:colorControlNormal">@color/colorControlNormal</item>
        <!--Button，textView的文字颜色-->
        <item name="android:textColor">@color/text_dark</item>
        <!--RadioButton checkbox等控件的文字-->
        <item name="android:textColorPrimaryDisableOnly">@color/text_dark</item>
        <!--默认按钮的背景颜色-->
        <item name="android:colorButtonNormal">@color/text_dark</item>
        <!--控件按压时的色调-->
        <item name="android:colorControlHighlight">@color/colorControlHighlight</item>
        <!--更多菜单的按钮样式-->
        <item name="android:actionOverflowButtonStyle">@style/ActionBarBaseStyle</item>
        <!--actionbar条目背景选择器-->
        <item name="android:actionBarItemBackground">@drawable/socialize_titlebar_item_background_selector</item>
        <!--actionbar条目菜单文本颜色-->
        <item name="android:actionMenuTextColor">@color/white</item>
        <!--弹出菜单listview的样式-->
        <item name="android:dropDownListViewStyle">@style/SpinnerDropDownListView</item>


         <!--title 标题栏字体设置-->
        <item name="android:titleTextAppearance">@style/MaterialAnimations.TextAppearance.Title</item>


        <item name="android:windowContentTransitions">true</item>
        <item name="android:windowAllowEnterTransitionOverlap">false</item>
        <item name="android:windowAllowReturnTransitionOverlap">false</item>
    </style>
    
    <style name="AppBlackTheme" parent="AppBaseTheme">
        <item name="colorPrimary">#3d3b3b</item>
        <item name="colorPrimaryDark">#151414</item>
        <item name="colorAccent">@color/colorAccent</item>
        <item name="image_sliding_block">@drawable/image_sliding_block_black</item>
    </style>


    <!--定义actionbar样式-->
    <style name="ActionBarBaseStyle" parent="@style/Widget.AppCompat.Light.ActionBar">
        <item name="background">@color/actionbar_background</item>
        <item name="titleTextStyle">@style/TitleStyle</item>
        <item name="android:icon">@android:color/transparent</item>
        <item name="subtitleTextStyle">@style/SubTitle</item>
    </style>

    <!--定义标题样式-->
    <style name="TitleStyle" parent="@style/TextAppearance.AppCompat.Widget.ActionBar.Title">
        <item name="android:textColor">@color/white</item>
    </style>

    <!--定义二级标题样式-->
    <style name="SubTitle" parent="@style/TextAppearance.AppCompat.Widget.ActionBar.Subtitle">
        <item name="android:textColor">@color/white</item>
    </style>

    <!--自定义actionbar 下拉菜单样式-->
    <style name="PopupMenu.ListPopupWindow" parent="Widget.AppCompat.Light.ListPopupWindow">
        <!--<item name="android:popupBackground">@color/menu_dropdown_panel_dark</item>-->
        <item name="android:textStyle">bold</item>
    </style>

    <!--自定义overflow样式-->
    <style name="OverflowButton" parent="Widget.AppCompat.ActionButton.Overflow">
        <item name="android:src">@mipmap/actionbar_more_icon_normal</item>
    </style>

    <!--自定义弹出菜单样式-->
    <style name="SpinnerDropDownListView" parent="@style/Widget.AppCompat.Light.ListView.DropDown">
        <item name="android:divider">#3f3f3f</item>
        <item name="android:dividerHeight">1dp</item>
    </style>

    <style name="mylistPopupWindowStyle" parent="@style/Widget.AppCompat.Light.PopupMenu">
        <item name="android:dropDownSelector">#343434</item>
        <item name="android:popupBackground">#343434</item>
    </style>

    <!-- app main menu style start! -->
    <!-- 菜单layout的样式 -->
    <style name="MenuItemLayoutStyle">
        <item name="android:layout_width">match_parent</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:minHeight">55dip</item>
        <item name="android:gravity">center_vertical</item>
        <item name="android:orientation">horizontal</item>
        <item name="android:paddingLeft">15dip</item>
        <item name="android:paddingRight">15dip</item>
        <item name="android:background">@drawable/drawer_menu_item_background</item>
    </style>

    <!-- 菜单ImageView的样式 -->
    <style name="MenuItemImageViewStyle">
        <item name="android:layout_width">24dip</item>
        <item name="android:layout_height">24dip</item>
        <item name="android:layout_marginRight">15dip</item>
    </style>

    <!-- 菜单TextView的样式 -->
    <style name="MenuItemTextViewStyle">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:textColor">@color/drawer_menu_text</item>
        <item name="android:drawablePadding">@dimen/space_10</item>
        <item name="android:textSize">@dimen/text_size_16</item>
    </style>
    <!-- app main menu style end! -->

    <!-- 操作项样式 start -->
    <style name="option_item_rl">
        <item name="android:layout_width">match_parent</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:background">@drawable/list_item_background</item>
        <item name="android:clickable">true</item>
        <item name="android:padding">@dimen/space_13</item>
        <item name="android:gravity">center_vertical</item>
        <item name="android:orientation">horizontal</item>
    </style>

    <style name="option_item_img">
        <item name="android:layout_width">28dp</item>
        <item name="android:layout_height">28dp</item>
        <item name="android:layout_marginRight">@dimen/space_10</item>
    </style>

    <style name="option_item_text_parent">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:layout_marginRight">@dimen/space_4</item>
        <item name="android:gravity">center_vertical</item>
        <item name="android:textColor">@color/main_black</item>
        <item name="android:clickable">false</item>
        <item name="android:layout_centerVertical">true</item>
        <item name="android:textSize">@dimen/text_size_16</item>
    </style>

    <style name="option_item_text" parent="@style/option_item_text_parent">
        <item name="android:drawablePadding">@dimen/space_8</item>
        <item name="android:textColor">#666</item>
    </style>

    <style name="option_item_text_fa" parent="@style/option_item_text_parent">
        <item name="android:layout_marginRight">10dp</item>
        <item name="android:textColor">@color/main_green</item>
        <item name="android:textSize">22sp</item>
    </style>

    <style name="option_item_goto_right">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:layout_alignParentRight">true</item>
        <item name="android:layout_centerVertical">true</item>
        <item name="android:src">@mipmap/ic_item_goto_right_tip</item>
        <item name="android:layout_marginRight">@dimen/space_10</item>
    </style>

    <style name="option_item_toggleButton">
        <item name="android:layout_width">45dp</item>
        <item name="android:layout_height">20dp</item>
    </style>

    <!-- 操作项样式end -->
    <style name="dialog_animation" parent="android:Animation">
        <item name="@android:windowEnterAnimation">@anim/dialog_enter</item>
        <item name="@android:windowExitAnimation">@anim/dialog_exit</item>
    </style>

    <style name="dialog_common" parent="Theme.AppCompat.Dialog">
        <item name="android:windowBackground">@drawable/dialog_background</item>
    </style>

    <style name="dialog_bottom" parent="@style/dialog_common">
        <item name="android:windowBackground">@drawable/dialog_bottom_background</item>
        <item name="android:windowAnimationStyle">@style/dialog_animation</item>
    </style>

    <!-- viewpage文本  滑动标签标题 -->
    <style name="viewpage_slidingTabTitle">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:gravity">center</item>
        <item name="android:textColor">@color/viewpage_selector_slide_title</item>
        <item name="android:textSize">17sp</item>
    </style>

    <!-- 加载滚动条样式 -->
    <style name="loading">
        <item name="android:indeterminate">true</item>
        <item name="android:indeterminateDrawable">@drawable/progressloading</item>
        <item name="android:indeterminateDuration">1000</item>
        <item name="android:indeterminateOnly">true</item>
    </style>

    <style name="wrap_view">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
    </style>

    <style name="fullline_view">
        <item name="android:layout_width">fill_parent</item>
        <item name="android:layout_height">wrap_content</item>
    </style>

    <style name="text_base" parent="@style/wrap_view">
        <item name="android:textSize">@dimen/text_regular_primary_size</item>
        <item name="android:textColor">@color/text_dark</item>
        <item name="android:ellipsize">end</item>
        <item name="android:maxLines">1</item>
        <item name="android:singleLine">true</item>
    </style>

    <style name="text_multiline" parent="@style/text_base">
        <item name="android:maxLines">5</item>
        <item name="android:singleLine">false</item>
        <item name="android:lineSpacingMultiplier">1.15</item>
    </style>

    <style name="dialog_divider">
        <item name="android:layout_gravity">bottom</item>
        <item name="android:background">@color/light_gray</item>
        <item name="android:layout_width">fill_parent</item>
        <item name="android:layout_height">1.0px</item>
        <item name="android:layout_alignParentBottom">true</item>
    </style>

    <style name="dialog_pinterest_text" parent="@style/text_multiline">
        <item name="android:textSize">@dimen/text_regular_primary_size</item>
        <item name="android:textColor">@color/text_dark</item>
        <item name="android:layout_width">fill_parent</item>
    </style>

    <style name="dialog_subtitle" parent="@style/fullline_view">
        <item name="android:textSize">@dimen/text_large_secondary_size</item>
        <item name="android:textColor">@color/text_light</item>
        <item name="android:gravity">center_vertical</item>
        <item name="android:maxLines">2</item>
        <item name="android:lineSpacingMultiplier">1.2</item>
    </style>

    <style name="dialog_text">
        <item name="android:textSize">@dimen/text_large_secondary_size</item>
        <item name="android:textColor">@color/text_light</item>
        <item name="android:layout_width">fill_parent</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:layout_marginBottom">@dimen/global_dialog_padding</item>
        <item name="android:lineSpacingMultiplier">1.3</item>
    </style>

    <style name="dialog_title" parent="@style/fullline_view">
        <item name="android:textSize">@dimen/text_large_primary_size</item>
        <item name="android:textStyle">bold</item>
        <item name="android:textColor">@color/text_dark</item>
        <item name="android:gravity">center_vertical</item>
    </style>

    <style name="list_cell_text">
        <item name="android:textSize">16.0dip</item>
        <item name="android:textColor">@color/white</item>
        <item name="android:ellipsize">end</item>
        <item name="android:gravity">center_vertical</item>
        <item name="android:layout_width">fill_parent</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:maxLines">1</item>
        <item name="android:singleLine">true</item>
    </style>

    <style name="list_cell_text_dialog" parent="@style/list_cell_text">
        <item name="android:textSize">16.0dip</item>
        <item name="android:textColor">@color/ui_dialog_list_text</item>
    </style>

    <style name="list_cell_divider">
        <item name="android:layout_gravity">bottom</item>
        <item name="android:background">#cccccc</item>
        <item name="android:layout_width">fill_parent</item>
        <item name="android:layout_height">1.0px</item>
        <item name="android:layout_alignParentBottom">true</item>
    </style>



    <style name="quick_option_item">
        <item name="android:layout_width">0dp</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:layout_weight">1</item>
        <item name="android:gravity">center_horizontal</item>
        <item name="android:orientation">vertical</item>
        <item name="android:padding">@dimen/space_16</item>
        <item name="android:background">@drawable/list_item_background</item>
    </style>

    <style name="quick_option_item_text">
        <item name="android:layout_width">wrap_content</item>
        <item name="android:layout_height">wrap_content</item>
        <item name="android:layout_marginTop">@dimen/space_12</item>
        <item name="android:textColor">@color/drawer_menu_text</item>
        <item name="android:textSize">@dimen/text_size_12</item>
    </style>


    <style name="quick_option_dialog" parent="@style/dialog_common">
        <!-- 背景 是否 全透明-->
        <item name="android:backgroundDimEnabled">true</item>
        <item name="android:windowBackground">@color/white40</item>
        <item name="android:windowAnimationStyle">@style/dialog_animation</item>
    </style>
    
    
#### -修改主题

    // 设置当前Activity的主题
    setTheme(R.style.AppBlackTheme);

    // 设置当前应用的主题
    getApplication().setTheme(R.style.AppBlackTheme);

    // 必须重新启动activity主题才生效		
    setTheme(R.style.AppBlackTheme);
    finish();
    startActivity(new Intent(this,MainActivity.class));

	private static int THEME = R.style.AppLightTheme;

	if(THEME != R.style.AppBlackTheme ){
			THEME = R.style.AppBlackTheme;
            finish();
            startActivity(new Intent(this,MainActivity.class));
			// 设置动画效果
			intent.setFlags(Intent.FLAG_ACTIVITY_NO_ANIMATION);
			overridePendingTransition(0, 0);
        }
			
    // 设置主题放到setContentView之前
    setTheme(R.style.AppBlackTheme);
    setContentView(R.layout.activity_main);
    
    
#### -窗口主题设置：（这里主要对于Activity设置，用到系统自动主题内容）


	android:theme=”@android:style/Theme.Dialog” 将一个Activity显示为能话框模式

	android:theme=”@android:style/Theme.NoTitleBar” 不显示应用程序标题栏

	android:theme=”@android:style/Theme.NoTitleBar.Fullscreen” 不显示应用程序标题栏，并全屏

	android:theme=”Theme.Light” 背景为白色

	android:theme=”Theme.Light.NoTitleBar” 白色背景并无标题栏

	android:theme=”Theme.Light.NoTitleBar.Fullscreen” 白色背景，无标题栏，全屏

	android:theme=”Theme.Black” 背景黑色

	android:theme=”Theme.Black.NoTitleBar” 黑色背景并无标题栏

	android:theme=”Theme.Black.NoTitleBar.Fullscreen” 黑色背景，无标题栏，全屏

	android:theme=”Theme.Wallpaper” 用系统桌面为应用程序背景

	android:theme=”Theme.Wallpaper.NoTitleBar” 用系统桌面为应用程序背景，且无标题栏

	android:theme=”Theme.Wallpaper.NoTitleBar.Fullscreen” 用系统桌面为应用程序背景，无标题栏，全屏

	android:theme=”Translucent” 半透明

	android:theme=”Theme.Translucent.NoTitleBar”

	android:theme=”Theme.Translucent.NoTitleBar.Fullscreen”

	android:theme=”Theme.Panel”

	android:theme=”Theme.Light.Panel”

    
