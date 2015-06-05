# Native React

## 约定
color: `5E97F6` `FF5E97F6` `0xFF5E97F6`

## 显示页面
> 示例:

```javascript
var DTNative = require('../apis/DTNative');
var options = {
  'action': 'show',
  'launchOptions': {
    'bundleURL': 'https://app.dingtalk.com/blackboard/main.jsbundle',
    'moduleName': 'Notice',
    'title': 'DingTalk',
    'barTintColor': 'FF5E97F6',
    'tintColor': 'FFFFFFFF',
    'titleTextColor': 'FFFFFFFF',
    'leftButtonTitle': '返回',
    'rightButtonTitle': '更多',
    'onRightButtonPress': 'onRightButtonPress1',
    'statusBarStyleLightContent': 'true',
    'presentMode': 'true',
  }
};
DTNative.callWithOptions(options);
```
                                                                
参数 | 值 | 描述 
--------- | ------- | ----------- 
action | show | 显示页面 
launchOptions | object | 加载参数

参数 | 类型 | 描述 | 必选
--------- | ------- | ----------- |--------
bundleURL | string | 网址 | true
moduleName | string | 导航栏标题 | true
title | string | 导航栏标题 | false
barTintColor | string | 导航栏背景颜色 | false
tintColor | string | 导航栏按钮颜色 | false
titleTextColor | string | 导航栏标题颜色 | false
leftButtonTitle | string | 导航栏左按钮文字 | false
rightButtonTitle | string | 导航栏右按钮文字 | false
onRightButtonPress | string | 导航栏右按钮事件标识 | false
statusBarStyleLightContent | bool | 设置白色状态栏 | false
presentMode | bool | 打开方式为push和present 默认push | false



## 关闭页面
> 示例:

```javascript
var DTNative = require('../apis/DTNative');
var options = {
  'action': 'dismiss',
};
DTNative.callWithOptions(options);
```

参数 | 值 | 描述 
--------- | ------- | ----------- 
action | dismiss | 关闭页面 

## 打开WebView
> 示例:

```javascript
var DTNative = require('../apis/DTNative');
var options = {
  'action': 'browse',
  'launchOptions': {
    'url': 'http://www.dingtalk.com/', 
    'title': 'DingTalk',
    'barTintColor': 'FF5E97F6',
    'tintColor': 'FFFFFFFF',
    'titleTextColor': 'FFFFFFFF',
    'leftButtonTitle': '返回',
    'rightButtonTitle': '更多',
    'onRightButtonPress': 'onRightButtonPress1',
    'statusBarStyleLightContent': 'true',
  }
};
DTNative.callWithOptions(options);
```

使用原生WebView加载                        
                                        
参数 | 值 | 描述 
--------- | ----------| ------ 
action | browse | WebView 
launchOptions | object | 加载参数

参数 | 类型 | 描述 | 必选
--------- | ------- | ------- | ----------
url | string | 网址 | true
title | string | 导航栏标题 | false
barTintColor | string | 导航栏背景颜色 | false
tintColor | string | 导航栏按钮颜色 | false
titleTextColor | string | 导航栏标题颜色 | false
leftButtonTitle | string | 导航栏左按钮文字 | false
rightButtonTitle | string | 导航栏右按钮文字 | false
onRightButtonPress | string | 导航栏右按钮事件标识 | false
statusBarStyleLightContent | bool | 设置白色状态栏 | false

## 公告模块
> 示例:

```javascript
var DTNative = require('../apis/DTNative');
var options = {
  'action': 'show',
  'launchOptions': {
    'corpid': 'qweasd', 
    'bundleURL': 'https://app.dingtalk.com/blackboard/main.jsbundle',
    'moduleName': 'Notice',
    'title': 'DingTalk',
    'barTintColor': 'FF5E97F6',
    'tintColor': 'FFFFFFFF',
    'titleTextColor': 'FFFFFFFF',
    'leftButtonTitle': '返回',
    'statusBarStyleLightContent': 'true',
  }
};
DTNative.callWithOptions(options);
```
                                                              
参数 | 值 | 描述 
--------- | ------- | ----------- 
action | pushVC | pushViewController
launchOptions | object | 加载参数

参数 | 类型 | 描述 | 必选
--------- | ------- | ----------- |--------
corpid | string | 企业ID | true
bundleURL | string | bundleURL | true
moduleName | string | 模块名 | true
title | string | 导航栏标题 | false
barTintColor | string | 导航栏按钮颜色 | false
tintColor | string | 导航栏按钮颜色 | false
titleTextColor | string | 导航栏标题颜色 | false
leftButtonTitle | string | 导航栏左按钮文字 | false
statusBarStyleLightContent | bool | 设置白色状态栏 | false