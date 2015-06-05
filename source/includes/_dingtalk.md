# APIS

##LWHttp
> 示例:

```javascript
var LWHttp = require('../apis/LWHttp');

LWHttp.get('http://www.dingtalk.com/data?ss=1', 'json', 10, (data) => {
	console.log(JSON.stringify(data));
});

```

请求网络数据只能使用该接口

参数 | 类型 | 描述 | 必选
--------- | ------- | ----------- |--------
url | string | 接口地址 | true
responseType | string | 返回类型 | true
timeout | int | 超时时间| true
callback | object | callback | false
		
##LWUrlUtils
> 示例:

```javascript
var LWUrlUtils = require('../apis/LWUrlUtils');
var url = LWUrlUtils.url('http://www.dingtalk.com/', 'login', {'corpid': corpid, 'offset': offset, 'limit': limit});
console.log(url);
```

参数 | 类型 | 描述 | 必选
--------- | ------- | ----------- |--------
host | string | host | true
path | string | path | true
params | object | {'corpid': corpid, 'offset': offset} | false
callback | object | callback | false

## DTFetch
> 示例:

```javascript
var DTFetch = require('../../dtbizs/DTFetch');

DTFetch.noticeList('QWESD', 1, 10, (data) => {
	console.log(JSON.stringify(data));
});


DTFetch.noticeDetail(1002, (data) => {
	console.log(JSON.stringify(data));
});

```

参数 | 类型 | 描述 | 必选
--------- | ------- | ----------- |--------
`noticeList`|||
corpid | string | 企业ID | true
offset | int | 偏移 | true
limit | int | 期望结果数量 | true
callback | object | callback | false
`noticeDetail` |||
参数 | 类型 | 描述 | 必选
bid | int | 公告ID | true
callback | object | callback | false

## DTError
> 示例:

```javascript
var DTError = require('../../dtbizs/DTError');
var error = DTError[1];
console.log(error.url);
console.log(error.msg);
```

Code | 描述
--------- | ------- 
-2 | {"url": "http://gtms02.alicdn.com/tps/i2/TB1hgeNHFXXXXc_XFXXojIlUFXX-277-276.png", "msg": "对不起\n暂时没有公告"}
-1 | {"url": "http://gtms03.alicdn.com/tps/i3/TB1feeeHFXXXXbiXFXXTyVt9VXX-128-128.png", "msg": "加载失败\n点击屏幕重试"}
20016 | {"url": "http://gtms02.alicdn.com/tps/i2/TB1hgeNHFXXXXc_XFXXojIlUFXX-277-276.png", "msg": "对不起\n您暂无权限查看该页面"}

## DTThirdPartyFetch

## DTThirdPartyError
