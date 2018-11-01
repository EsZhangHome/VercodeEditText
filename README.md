<img src="/img/VercodeEditTex.png" width="800px"/>

## Introduction
An android Verification code EditText.   
一个安卓验证码输入框控件。([中文版入口](README-CN.md))  
[![Platform](https://img.shields.io/badge/platform-android-green.svg)](http://developer.android.com/index.html)
<img src="https://img.shields.io/badge/license-Apache 2.0-green.svg?style=flat">
[![SDK](https://img.shields.io/badge/API-12%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=11)
![VercodeEditText](https://api.bintray.com/packages/jkb/maven/vercodeedittext/images/download.svg)

## Demo
Prevent input overflow.  
<img src="/img/demo.gif" width="280px"/>

## Features
- [x] **Extends EditText,it can be used as EditText**  
- [x] **Prevent input overflow**  
- [x] **Custom validation code length**  
- [x] **Provide input value listener**  
- [x] **Layout height is auto adjust**  
- [x] **Attributes can be configured for customization**  
- [x] **Custom cursor style**

## Version
name|VercodeEditText
---|---
latest|![VercodeEditText](https://api.bintray.com/packages/jkb/maven/vercodeedittext/images/download.svg)

## Configure
#### Maven
```xml
<dependency>
  <groupId>com.justkiddingbaby</groupId>
  <artifactId>vercodeedittext</artifactId>
  <version>the latest version</version>
  <type>pom</type>
</dependency>
```
#### JCenter
First. add to project build.gradle
```gradle
repositories {
    jcenter()
}
```
Second. add to module build.gradle
```gradle
'com.justkiddingbaby:vercodeedittext:the latest version'
```

## Attributes instruction
attribute|instruction|value
---|---|---
[figures](/vcedittext-lib/src/main/res/values/attrs.xml)|the verification code length|integer
[verCodeMargin](/vcedittext-lib/src/main/res/values/attrs.xml)|the padding for each verification code number|dimension
[bottomLineSelectedColor](/vcedittext-lib/src/main/res/values/attrs.xml)|the color of bottom line is select status|reference
[bottomLineNormalColor](/vcedittext-lib/src/main/res/values/attrs.xml)|the color of bottom line is normal status|reference
[bottomLineHeight](/vcedittext-lib/src/main/res/values/attrs.xml)|the height of bottom line|dimension
[selectedBackgroundColor](/vcedittext-lib/src/main/res/values/attrs.xml)|the background color of verification code is select status|reference
[cursorDuration](/vcedittext-lib/src/main/res/values/attrs.xml)|the duration of cursor blink|integer
[cursorColor](/vcedittext-lib/src/main/res/values/attrs.xml)|the color of cursor|integer
[cursorWidth](/vcedittext-lib/src/main/res/values/attrs.xml)|the width of cursor|integer

## Function instruction
return|function name|instruction
---|---|---
void|[setFigures(int figures)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the verification code length
void|[setVerCodeMargin(int margin)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the padding for each verification code number
void|[setBottomSelectedColor(int bottomSelectedColor)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the color of bottom line is select status
void|[setBottomNormalColor(int bottomNormalColor)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the color of bottom line is normal status
void|[setSelectedBackgroundColor(int selectedBackground)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the background color of verification code is select status
void|[setBottomLineHeight(int bottomLineHeight)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|set the height of bottom line
void|[setOnVerificationCodeChangedListener(OnVerificationCodeChangedListener listener)](/vcedittext-lib/src/main/java/com/jkb/vcedittext/VerificationAction.java)|add the listener when verification value is changing|

## Usage
#### use in the layout
```xml
  <com.jkb.vcedittext.VerificationCodeEditText
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:inputType="number"
        android:text="123"
        android:textColor="@color/colorPrimary"
        android:textSize="40sp"
        app:bottomLineHeight="2dp"
        app:bottomLineNormalColor="@color/gravy_light"
        app:bottomLineSelectedColor="@color/colorAccent"
        app:figures="4"
        app:selectedBackgroundColor="@color/colorPrimary_alpha33"
        app:verCodeMargin="10dp" />
 ```
 
## Release history
#### v1.1.0 (2018/11/1)
1、Add cursor support.
#### v1.0.5(2017/12/5)
1、Fix the bug that could appear when the view is pressed.
#### v1.0.4(2017/10/14)
1、Remove label element at AndroidManifest.xml.  
#### v1.0.3(2017/8/15)
1、make interface class VerificationAction public.  
#### v1.0.2(2017/6/29)
1、Fix the conflict that allowBackup property is false under the application in AndroidMainfet.xml file.  
#### v1.0.1(2017/6/27)
1、fix bug:can't get focus when the view is touched.
#### v1.0.0(2017/6/12)
1、release VercodeEditText，Prevent input overflow.  
2、Encapsulation demo.
