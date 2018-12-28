# 广告请求和返回json示例

- [广告请求和返回json示例](#%E5%B9%BF%E5%91%8A%E8%AF%B7%E6%B1%82%E5%92%8C%E8%BF%94%E5%9B%9Ejson%E7%A4%BA%E4%BE%8B)
	- [banner](#banner)
		- [banner请求示例](#banner%E8%AF%B7%E6%B1%82%E7%A4%BA%E4%BE%8B)
		- [banner图片广告返回示例](#banner%E5%9B%BE%E7%89%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [banner广告展示示例](#banner%E5%B9%BF%E5%91%8A%E5%B1%95%E7%A4%BA%E7%A4%BA%E4%BE%8B)
		- [banner图文广告返回示例](#banner%E5%9B%BE%E6%96%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [测试返回广告示例](#%E6%B5%8B%E8%AF%95%E8%BF%94%E5%9B%9E%E5%B9%BF%E5%91%8A%E7%A4%BA%E4%BE%8B)
		- [banner html返回示例](#banner-html%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [banner广告html返回示例](#banner%E5%B9%BF%E5%91%8Ahtml%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
	- [插屏](#%E6%8F%92%E5%B1%8F)
		- [插屏请求示例](#%E6%8F%92%E5%B1%8F%E8%AF%B7%E6%B1%82%E7%A4%BA%E4%BE%8B)
		- [插屏图片广告返回示例](#%E6%8F%92%E5%B1%8F%E5%9B%BE%E7%89%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [APP中插屏图片广告返回示例](#app%E4%B8%AD%E6%8F%92%E5%B1%8F%E5%9B%BE%E7%89%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
		- [插屏图文广告返回示例](#%E6%8F%92%E5%B1%8F%E5%9B%BE%E6%96%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [插屏图文广告返回示例](#%E6%8F%92%E5%B1%8F%E5%9B%BE%E6%96%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
		- [插屏html广告返回示例](#%E6%8F%92%E5%B1%8Fhtml%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
		- [插屏可玩广告返回示例](#插屏可玩广告返回示例)
		- [插屏视频广告返回示例](#插屏视频广告返回示例)
	- [开屏](#%E5%BC%80%E5%B1%8F)
		- [开屏请求示例](#%E5%BC%80%E5%B1%8F%E8%AF%B7%E6%B1%82%E7%A4%BA%E4%BE%8B)
			- [开屏图片广告返回示例](#%E5%BC%80%E5%B1%8F%E5%9B%BE%E7%89%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
		- [开屏图文广告返回示例](#%E5%BC%80%E5%B1%8F%E5%9B%BE%E6%96%87%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
		- [开屏html广告返回示例](#%E5%BC%80%E5%B1%8Fhtml%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
	- [原生广告](#%E5%8E%9F%E7%94%9F%E5%B9%BF%E5%91%8A)
		- [原生广告请求示例](#%E5%8E%9F%E7%94%9F%E5%B9%BF%E5%91%8A%E8%AF%B7%E6%B1%82%E7%A4%BA%E4%BE%8B)
			- [原生广告返回示例](#%E5%8E%9F%E7%94%9F%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
	- [视频广告](#%E8%A7%86%E9%A2%91%E5%B9%BF%E5%91%8A)
		- [视频广告请求示例](#%E8%A7%86%E9%A2%91%E5%B9%BF%E5%91%8A%E8%AF%B7%E6%B1%82%E7%A4%BA%E4%BE%8B)
			- [视频广告返回示例](#%E8%A7%86%E9%A2%91%E5%B9%BF%E5%91%8A%E8%BF%94%E5%9B%9E%E7%A4%BA%E4%BE%8B)
			- [视频可玩广告返回示例](#视频可玩广告返回示例)

> - 示例中可以使用：
> 
> 测试Token为``EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=`` 

> 测试APP 参数：

| OS | APP ID | Slot Format | Slot ID |
| ----- | ----- | ----- | ----- |
| Android | bg76gil7 | banner | an6o1ngv |
| Android | bg76gil7 | Interstitial | 13ohe4ze |
| Android | bg76gil7 | Reawrd Video | dsdibu5j |
| Android | bg76gil7 | Native | 13ur17b0 |
| Android | bg76gil7 | Splash | 50otuc9h |
| iOS | yywtptfq | banner | 5jr45zcy |
| iOS | yywtptfq | Interstitial | n0w2zkex |
| iOS | yywtptfq | Reawrd Video | hmtdjpt4 |
| iOS | yywtptfq | Native | gk8cmfh8 |
| iOS | yywtptfq | Splash | ss03ye17 |


> - 作为测试token获取测试数据，供测试查看效果使用，正式上线后请切换为正式的Token及APP ID，否则将不会产生任何请求，展示，点击收益等数据。
> - 返回信息的主要错误类型及说明：-1：参数值类型错误；-3：无广告填充；-4：该流量被屏蔽（反作弊）；-5：字段校验失败/字段非法。

## banner

### banner请求示例

``` json

	{
	    "ver": "1.1",
	    "ssp_token": "zplay提供的ssp_token",
	    "need_https": 0,
	    "app": {
	        "id": "zplay提供的app_id",
	        "name": "DrivingTest",
	        "app_key": "zplay提供的app_key",
	        "bundle": "cn.eclicks.drivingtest",
	        "ver": "",
	        "cat": []
	    },
	    "device": {
	        "model": "MHA-AL00",
	        "brand": "HUAWEI",
	        "adt": 1,
	        "connection_type": "wifi",
	        "carrier": 0,
	        "orientation": 1,
	        "mac": "84:be:52:7a:24:67",
	        "imei": "862552036260906",
	        "android_id": "5588e0a238461ee8",
	        "openudid": "5e8061c7-1079-35d2-a218-c4aa739f7870",
	        "os_type": "android",
	        "os_version": "7.0",
	        "screen": {
	            "w": 1080,
	            "h": 1812,
	            "dpi": 480
	        },
	        "geo": {
	            "lat": 29.22145,
	            "lon": 119.84023
	        }
	    },
	    "ads": [
	        {
	            "type": 0,
	            "place_id": "an6o1ngv",
	            "floor_price": 100,
	            "currency": "CNY",
	            "w": 640,
	            "h": 100,
	            "inventory_types": [
	                1,
	                2,
	                4,
	                5
	            ]
	        }
	    ]
	}
```

### banner图片广告返回示例

> 如果请求参数 `inventory_types:[]` 中包含 `1(物料类型为图片)`，则玉米广告可以返回图片广告，返回参数中 `inventory_type` 也会标为 `1`，代表此广告为图片类型的广告。

```json

	{
	    "ads": [
	        {
	            "id": "464",
	            "place_id": "",
	            "action": 2,
	            "image_url": "http://pgdt.gtimg.cn/gdt/0/DAACinJAJYAH0ABJBWoebKBuOgTF8e.jpg/0?ck=13afb5e35954c59df6d0027ac679eb91",
	            "w": 720,
	            "h": 1038,
	            "target_url": "http://c.gdt.qq.com/gdt_mclick.fcg?viewid=t6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu!!XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q!9A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_!csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg&jtype=0&i=1&os=2",
	            "click_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=1dfd3ecd691b73d7&t=1&bid_id=0bts0K1CObXU1MkqKd28U76h45LrcY&ad_id=464&type=2&dsp_id=20&plmn=46000&ssp_id=449&app_id=1007877&app_bundle_id=cn.eclicks.drivingtest&price_enc=Xm7JWFA9pOhXsloDA1CMNw&cur=CNY&u=http%3A%2F%2Fc.gdt.qq.com%2Fgdt_mclick.fcg%3Fviewid%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg%26jtype%3D0%26i%3D1%26os%3D2%3Fviewid%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg%26acttype%3D1%26s%3D%257B%2522down_x%2522%253A0%252C%2522down_y%2522%253A0%257D&adid_sha1=&aid_sha1=67d3bc8ba4a697f34c7165779438873896665f3e&pid=zap937e286143f6d462185316171ff574a7b10077f6"
	            ],
	            "imp_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=607f65d9268021d3&t=0&bid_id=0bts0K1CObXU1MkqKd28U76h45LrcY&ad_id=464&type=2&dsp_id=20&plmn=46000&ssp_id=449&app_id=1007877&app_bundle_id=cn.eclicks.drivingtest&price_enc=Xm7JWFA9pOhXsloDA1CMNw&cur=CNY&u=http%3A%2F%2Fv.gdt.qq.com%2Fgdt_stats.fcg%3Fcount%3D1%26viewid0%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg&adid_sha1=&aid_sha1=67d3bc8ba4a697f34c7165779438873896665f3e&pid=zap937e286143f6d462185316171ff574a7b10077f6"
	            ],
	            "refresh_interval": 90,
	            "inventory_type": 1,
	            "ssp_id": "9",
	            "ex_param": [
	                "",
	                "",
	                "",
	                "",
	                ""
	            ],
	            "price": 0
	        }
	    ],
	    "msg": "",
	    "result": 0
	}
```

#### banner广告展示示例

![banner](/img/banner_img1.jpg)

### banner图文广告返回示例

> 如果请求参数 `inventory_types:[]` 中包含 `2(物料类型为图文)` ，则玉米广告可以返回图文广告，返回参数中 `inventory_type` 也会标为 `2`，代表此广告为图文类型的广告，图文广告返回的title和desc字段会有对应的标题和描述。

```json

	{
	  "ads": [
	    {
	      "id": "12345",
	      "place_id": "",
	      "action": 2,
	      "image_url": "http://ppgz.zplay.cn/image/adx_img/64-64.png",
	      "w": 728,
	      "h": 90,
	      "app_bundle": "com.zplay.cn",
	      "target_url": "http://www.zplay.cn",
	      "click_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=ef04cd9d5fb26ac&t=1&bid_id=0bts0I1COlE84eWliQ0acOvq1BuEwD&ad_id=12345&type=0&dsp_id=129&plmn=46002&ssp_id=1&app_id=1006896&app_bundle_id=com.zplay.android.sdk.zplayad.demo1302&price_enc=vP_JWAZgp3pIO4IGGREl0g&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=&aid_sha1=dd1f217060dc909168c1c8642525bb24765c2e09&test=1&pid=zapdd13a671432d4a653e372fa03b3c68971f788a12",
	        "http://test.adx.yumimobi.com/page_click.php"
	      ],
	      "imp_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=116c574d39434e0d&t=0&bid_id=0bts0I1COlE84eWliQ0acOvq1BuEwD&ad_id=12345&type=0&dsp_id=129&plmn=46002&ssp_id=1&app_id=1006896&app_bundle_id=com.zplay.android.sdk.zplayad.demo1302&price_enc=vP_JWAZgp3pIO4IGGREl0g&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=&aid_sha1=dd1f217060dc909168c1c8642525bb24765c2e09&test=1&pid=zapdd13a671432d4a653e372fa03b3c68971f788a12",
	        "http://test.adx.yumimobi.com/page_show.php"
	      ],
	      "refresh_interval": 0,
	      "inventory_type": 2,
	      "title": "长腿爸爸",
	      "desc": "一个非常好玩的亲子游戏，快来体验吧",
	      "ssp_id": "10",
	      "price": 0
	    }
	  ],
	  "msg": "",
	  "result": 0
	}
```

> 图文广告不能像图片广告一样，直接把image_url图片展示出来，通常是将图片，标题，描述按照左图右文字（标题上，描述下或标题描述拼接在一起）组合拼装，如下面示例；媒体也可以根据自己的需求选择拼接的样式。

#### 测试返回广告示例

![test2](/img/banner-pic-test2.jpg)

### banner html返回示例

> 如果请求参数 `inventory_types:[]` 中包含 `4(物料类型为html)`,则表示媒体支持html广告展示，玉米广告可以返回html广告，返回参数中 `inventory_type` 也会标为 `4`，代表此广告为html类型的广告，html_snippet字段中即为需要展示的html代码段。

```json

	{
	  "ads": [
	    {
	      "id": "12345",
	      "place_id": "",
	      "action": 2,
	      "html_snippet": "<!DOCTYPE html><html><head><meta charset=\"utf-8\"/><meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no,telephone=no\"/><meta name=\"format-detection\" content=\"telephone=no\"/><title></title><style>html,body{width:100%;height:100%;}*{padding:0;margin:0}img{display:block;position:absolute;top:0;left:0;width:100% !important;height:100% !important;}img[width=\"1\"]{width:1px;height:1px;display:none}img[width=\"1px\"]{width:1px;height:1px;display:none}img[width=\"0\"]{width:1px;height:1px;display:none}img[width=\"0px\"]{width:1px;height:1px;display:none}</style></head><body><div id=\"container\"><div class=\"veiw_con\"><a href=\"https://lnk0.com/NZ5E50?clickFlag=zplay\"><img id=\"img2\" class=\"com-img\" src=\"http://cdn.f2time.com/image/20161205/1e134d003ce34f9693a768abc2994928_tmp.jpg\"/></a></div></div></body></html>",
	      "image_url": "",
	      "w": 320,
	      "h": 50,
	      "app_bundle": "com.zplay.cn",
	      "target_url": "http://www.zplay.cn",
	      "click_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=42aff45315acb70d&t=1&bid_id=0bug6s1COrdw4rZwoY1AtZst4npvg3&ad_id=12345&type=0&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=YlPKWATzcV8O4PyFuQc7Kw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap64366690d9b306604610228a465db1aa97e42e89",
	        "http://test.adx.yumimobi.com/page_click.php"
	      ],
	      "imp_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=699706254edd7d40&t=0&bid_id=0bug6s1COrdw4rZwoY1AtZst4npvg3&ad_id=12345&type=0&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=YlPKWATzcV8O4PyFuQc7Kw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap64366690d9b306604610228a465db1aa97e42e89",
	        "http://test.adx.yumimobi.com/page_show.php"
	      ],
	      "refresh_interval": 0,
	      "inventory_type": 4,
	      "ssp_id": "10",
	      "price": 0
	    }
	  ],
	  "msg": "",
	  "result": 0
	}
```

> 媒体看到返回的 `invenroy为4` 时，直接将 `html_snippet` 中的代码段内容在APP中渲染出来即可。html广告中 `image_url` 字段是空的，可以忽略。

#### banner广告html返回示例


![banner_html](/img/banner_html_ad.PNG)

## 插屏

### 插屏请求示例

> 同banner广告一样，插屏广告在请求的时候也需要通过 `inventory_types` 标明支持的物料类型

```json

	{
	    "ver": "1.1",
	    "ssp_token": "zplay提供的ssp_token",
	    "need_https": 0,
	    "app": {
	        "id": "zplay提供的app_id",
	        "name": "DrivingTest",
	        "app_key": "zplay提供的app_key",
	        "bundle": "cn.eclicks.drivingtest",
	        "ver": "",
	        "cat": []
	    },
	    "device": {
	        "model": "vivoX7",
	        "brand": "vivo",
	        "adt": 1,
	        "connection_type": "wifi",
	        "carrier": 0,
	        "orientation": 1,
	        "mac": "20:5d:47:0b:33:38",
	        "imei": "862505031462331",
	        "android_id": "840be0b0d00e6169",
	        "openudid": "e4791d89-dda9-36c0-b9df-edacc24b01c8",
	        "os_type": "android",
	        "os_version": "5.1.1",
	        "screen": {
	            "w": 1080,
	            "h": 1920,
	            "dpi": 480
	        },
	        "geo": {
	            "lat": 31.151308,
	            "lon": 108.36747
	        }
	    },
	    "ads": [
	        {
	            "type": 1,
	            "place_id": "13ohe4ze",
	            "floor_price": 100,
	            "currency": "CNY",
	            "w": 720,
	            "h": 1038,
	            "inventory_types": [
	                1,
	                2,
	                4,
	                5
	            ]
	        }
	    ]
	}
```

### 插屏图片广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持图片广告，且返回的广告中 `invenroy_type` 为1，则媒体将 `img_url` 图片展示出来即可。

```json

	{
	  "ads": [
	    {
	      "id": "12345",
	      "place_id": "",
	      "action": 2,
	      "image_url": "http://ppgz.zplay.cn/image/adx_img/640x960.jpg",
	      "w": 640,
	      "h": 960,
	      "app_bundle": "com.zplay.cn",
	      "target_url": "http://www.zplay.cn",
	      "click_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=73cc52f1feb1da5e&t=1&bid_id=0bts0K1COs1I0y4BSv1bbpHN3VyPRY&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=il_KWNyfsheu7FYW3m3eLw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
	        "http://test.adx.yumimobi.com/page_click.php"
	      ],
	      "imp_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=6af77c9ef310cdb1&t=0&bid_id=0bts0K1COs1I0y4BSv1bbpHN3VyPRY&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=il_KWNyfsheu7FYW3m3eLw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
	        "http://test.adx.yumimobi.com/page_show.php"
	      ],
	      "refresh_interval": 0,
	      "inventory_type": 1,
	      "ssp_id": "10",
	      "price": 0
	    }
	  ],
	  "msg": "",
	  "result": 0
	}
```

#### APP中插屏图片广告返回示例

![interstitial_picture](/img/intersitial_pic_1.PNG)

### 插屏图文广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持图文广告，且返回的广告中 `invenroy_type` 为2，则改广告位图文广告。（图文广告通常图片为小图ICON）

```json

	{
	  "ads": [
	    {
	      "id": "12345",
	      "place_id": "",
	      "action": 2,
	      "image_url": "http://ppgz.zplay.cn/image/adx_img/64-64.png",
	      "w": 640,
	      "h": 960,
	      "app_bundle": "com.zplay.cn",
	      "target_url": "http://www.zplay.cn",
	      "click_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=1caadc2eca3cdf3a&t=1&bid_id=0bulZf1COwg645eaAm0q12Wl0KQyQc&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=Fp_KWHCqskhzQOB8UEukkQ&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
	        "http://test.adx.yumimobi.com/page_click.php"
	      ],
	      "imp_trackers": [
	        "http://stat.adx.yumimobi.com/api/s?r=7d7b2ba2193af5f1&t=0&bid_id=0bulZf1COwg645eaAm0q12Wl0KQyQc&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=Fp_KWHCqskhzQOB8UEukkQ&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
	        "http://test.adx.yumimobi.com/page_show.php"
	      ],
	      "refresh_interval": 0,
	      "inventory_type": 2,
	      "title": "长腿爸爸",
	      "desc": "一个非常好玩的亲子游戏，快来体验吧",
	      "ssp_id": "10",
	      "price": 0
	    }
	  ],
	  "msg": "",
	  "result": 0
	}
```

> 同banner的图文广告一样,不能只将 `img_url` 图片展示出来，需要将 `img_url` `title` `desc` 字段按照一定的格式排列组织好，展示出来即可，即可参照下图的示例来排列展示，也可以由媒体自己来组织展现方式。

### 插屏图文广告返回示例

![interstitial_pic_text](/img/intersitial_pic_text.PNG)

### 插屏html广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持html广告，即包含4，且返回的广告中 `invenroy_type` 为4，则该广告为插屏的html广告。展示方式同banner的html广告，请参考banner html广告展示。

### 插屏可玩广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持可玩广告，即包含10，且返回的广告中 `invenroy_type` 为10，则该广告为插屏的可玩广告。可玩广告是可以交互操作的html，并填充到html_snippet参数中。

```json
{
    "ads": [
        {
            "id": "12345",
            "place_id": "",
            "action": 6,
            "html_snippet": "<!DOCTYPE html>\n<html>\n  <head>\n    <meta name=\"viewport\" content=\"user-scalable=no, width=device-width, initial-scale=1, maximum-scale=1\">\n    <title>Atmosplayer</title>\n    <meta charset=\"utf-8\"/>\n    <script>\n      window.gestures = [\n  [\n    {\n      \"id\": 0,\n      \"type\": \"tap\",\n      \"attack\": 0,\n      \"target\": 1999,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": false,\n      \"tapDirection\": 1,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 1,\n      \"type\": \"tap\",\n      \"attack\": 3269,\n      \"loopStart\": 4368,\n      \"target\": 6519,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.5544973544973544,\n          \"y\": 0.5595238095238095,\n          \"width\": 0.33015873015873015,\n          \"height\": 0.15\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 2,\n      \"type\": \"tap\",\n      \"attack\": 7458,\n      \"loopStart\": 8355,\n      \"target\": 10357,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.6476190476190475,\n          \"y\": 0.5952380952380952,\n          \"width\": 0.3386243386243386,\n          \"height\": 0.20714285714285716\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 3,\n      \"type\": \"tap\",\n      \"attack\": 11913,\n      \"loopStart\": 12863,\n      \"target\": 14913,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.45291005291005293,\n          \"y\": 0.5880952380952381,\n          \"width\": 0.182010582010582,\n          \"height\": 0.20952380952380953\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 4,\n      \"type\": \"tap\",\n      \"attack\": 15849,\n      \"loopStart\": 16643,\n      \"target\": 18849,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.30052910052910053,\n          \"y\": 0.5904761904761905,\n          \"width\": 0.2455026455026455,\n          \"height\": 0.19047619047619047\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 5,\n      \"type\": \"tap\",\n      \"attack\": 19786,\n      \"loopStart\": 20736,\n      \"target\": 22736,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.35555555555555557,\n          \"y\": 0.5952380952380952,\n          \"width\": 0.16507936507936508,\n          \"height\": 0.20952380952380953\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 6,\n      \"type\": \"tap\",\n      \"attack\": 23722,\n      \"loopStart\": 24472,\n      \"target\": 26572,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.09312169312169312,\n          \"y\": 0.4976190476190476,\n          \"width\": 0.30052910052910053,\n          \"height\": 0.14523809523809525\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 7,\n      \"type\": \"tap\",\n      \"attack\": 27348,\n      \"loopStart\": 28448,\n      \"target\": 30398,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.10158730158730159,\n          \"y\": 0.530952380952381,\n          \"width\": 0.31322751322751324,\n          \"height\": 0.1\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 8,\n      \"type\": \"tap\",\n      \"attack\": 31284,\n      \"loopStart\": 32134,\n      \"target\": 34129,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.15661375661375662,\n          \"y\": 0.6238095238095238,\n          \"width\": 0.1693121693121693,\n          \"height\": 0.16666666666666666\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 9,\n      \"type\": \"tap\",\n      \"attack\": 34776,\n      \"loopStart\": 35676,\n      \"target\": 37876,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.2074074074074074,\n          \"y\": 0.6261904761904762,\n          \"width\": 0.25396825396825395,\n          \"height\": 0.16666666666666666\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 10,\n      \"type\": \"tap\",\n      \"attack\": 38847,\n      \"loopStart\": 39647,\n      \"target\": 41747,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.9523809523809523,\n          \"y\": 0.4666666666666667,\n          \"width\": 0.16084656084656085,\n          \"height\": 0.23333333333333334\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 11,\n      \"type\": \"tap\",\n      \"attack\": 42576,\n      \"loopStart\": 43276,\n      \"target\": 45526,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.5037037037037037,\n          \"y\": 0.6833333333333333,\n          \"width\": 0.2582010582010582,\n          \"height\": 0.14761904761904762\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 12,\n      \"type\": \"tap\",\n      \"attack\": 46513,\n      \"loopStart\": 47363,\n      \"target\": 49413,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.5037037037037037,\n          \"y\": 0.7452380952380953,\n          \"width\": 0.23703703703703702,\n          \"height\": 0.14761904761904762\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 13,\n      \"type\": \"tap\",\n      \"attack\": 50242,\n      \"loopStart\": 50942,\n      \"target\": 53192,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.10582010582010581,\n          \"y\": 0.8119047619047619,\n          \"width\": 0.26666666666666666,\n          \"height\": 0.1619047619047619\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 14,\n      \"type\": \"tap\",\n      \"attack\": 54075,\n      \"loopStart\": 54725,\n      \"target\": 57025,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.7068783068783069,\n          \"y\": 0.7690476190476191,\n          \"width\": 0.2751322751322751,\n          \"height\": 0.1\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 15,\n      \"type\": \"tap\",\n      \"attack\": 57701,\n      \"loopStart\": 58751,\n      \"target\": 60751,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.656084656084656,\n          \"y\": 0.8738095238095238,\n          \"width\": 0.17354497354497356,\n          \"height\": 0.1619047619047619\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 16,\n      \"type\": \"tap\",\n      \"attack\": 61534,\n      \"loopStart\": 62184,\n      \"target\": 64531,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.9566137566137566,\n          \"y\": 0.8928571428571429,\n          \"width\": 0.3216931216931217,\n          \"height\": 0.29523809523809524\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 17,\n      \"type\": \"tap\",\n      \"attack\": 65574,\n      \"loopStart\": 66220,\n      \"target\": 68473,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.9396825396825397,\n          \"y\": 0.9476190476190476,\n          \"width\": 0.30052910052910053,\n          \"height\": 0.16428571428571428\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 18,\n      \"type\": \"tap\",\n      \"attack\": 69407,\n      \"loopStart\": 70307,\n      \"target\": 72307,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.8,\n          \"y\": 0.8714285714285714,\n          \"width\": 0.2582010582010582,\n          \"height\": 0.15\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 19,\n      \"type\": \"tap\",\n      \"attack\": 73186,\n      \"loopStart\": 73786,\n      \"target\": 76136,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.9396825396825397,\n          \"y\": 0.9428571428571428,\n          \"width\": 0.30476190476190484,\n          \"height\": 0.14285714285714285\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 20,\n      \"type\": \"tap\",\n      \"attack\": 77283,\n      \"loopStart\": 77933,\n      \"target\": 80083,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.656084656084656,\n          \"y\": 0.930952380952381,\n          \"width\": 0.5417989417989418,\n          \"height\": 0.15\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 21,\n      \"type\": \"tap\",\n      \"attack\": 81734,\n      \"loopStart\": 82484,\n      \"target\": 84684,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.7576719576719577,\n          \"y\": 0.8666666666666667,\n          \"width\": 0.19894179894179895,\n          \"height\": 0.1619047619047619\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 22,\n      \"type\": \"tap\",\n      \"attack\": 85567,\n      \"loopStart\": 86417,\n      \"target\": 88517,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.8465608465608465,\n          \"y\": 0.8738095238095238,\n          \"width\": 0.1693121693121693,\n          \"height\": 0.1738095238095238\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 23,\n      \"type\": \"tap\",\n      \"attack\": 89296,\n      \"loopStart\": 90246,\n      \"target\": 92296,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.28359788359788357,\n          \"y\": 0.9714285714285714,\n          \"width\": 0.42328042328042326,\n          \"height\": 0.11666666666666667\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 24,\n      \"type\": \"tap\",\n      \"attack\": 93233,\n      \"loopStart\": 94183,\n      \"target\": 96183,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.7576719576719577,\n          \"y\": 0.9619047619047619,\n          \"width\": 0.3682539682539683,\n          \"height\": 0.10238095238095238\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 25,\n      \"type\": \"tap\",\n      \"attack\": 97066,\n      \"loopStart\": 97916,\n      \"target\": 100016,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.5502645502645502,\n          \"y\": 0.9428571428571428,\n          \"width\": 0.18624338624338624,\n          \"height\": 0.19047619047619047\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 26,\n      \"type\": \"tap\",\n      \"attack\": 100849,\n      \"loopStart\": 101499,\n      \"target\": 103699,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.050793650793650794,\n          \"y\": 0.8785714285714286,\n          \"width\": 0.18624338624338624,\n          \"height\": 0.17142857142857143\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ],\n  [\n    {\n      \"id\": 27,\n      \"type\": \"tap\",\n      \"attack\": 104524,\n      \"loopStart\": 105124,\n      \"target\": 107424,\n      \"fullscreen\": false,\n      \"shapes\": [\n        {\n          \"type\": \"square\",\n          \"x\": 0.09312169312169312,\n          \"y\": 0.9642857142857143,\n          \"width\": 0.2920634920634921,\n          \"height\": 0.10714285714285714\n        }\n      ],\n      \"mandatory\": true,\n      \"tapDirection\": 2,\n      \"loop\": true,\n      \"tapCount\": 1\n    }\n  ]\n];\n      window.showUserGuide = false;\n      window.userGuideUrl = 'undefined';\n      window.userGuidePosition = {};\n      window.installAttributes = {\"x\":0.269510177064372,\"y\":0.007142857142857143,\"width\":0.4821611782227371,\"percentage\":true};\n      window.showFloatingMenu = true;\n      window.videoOrientation = 0;\n      window.disableUserFeedback = false;\n\n      window.hasEndCard = false;\n      window.endCardSettings = undefined;\n      \n      \n    </script>\n  </head>\n  <body>\n    <div id=\"mainContainer\">\n      <img id=\"loadingImage\" src=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/load.jpg\" />\n      <div id=\"rotatedContainer\">\n\n        <img id=\"closeButton\" src=\"https://adcdn.zplayads.com/assets/images/x_button.png\"/>\n        <img id=\"restartButton\" src=\"https://adcdn.zplayads.com/assets/images/restart.png\"/>\n\n        <img id=\"installButton\" src=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/downloadImage.png?key=468\" />\n\n        <video id=\"atmosPlayer\" webkit-playsinline playsinline muted preload=\"auto\" src=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/transcoded_video_1500kbps.mp4\" poster=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/load.jpg\" autoplay></video>\n        <audio id=\"bgMusicPlayer\" src=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/bgMusic.mp3?key=744\" type=\"audio/mpeg\" loop></audio>\n\n        <video id=\"atmosPlayerEndCard\" webkit-playsinline playsinline muted preload=\"auto\" src=\"\" poster=\"https://adcdn.zplayads.com/assets/prod/6ea73ab0-3cc4-11e8-a313-55140a049e95/load.jpg\" style=\"z-index: -10;\"></video>\n\n        <canvas id=\"gestureDetector\"></canvas>\n        <canvas id=\"userFeedback\"></canvas>\n\n        <div id=\"floatingMenu\" class=\"simple\">\n          <span class=\"title\">¿ÉÍæµÄÃÔÄãÓÎÏ·</span><img alt=\"gamebox\" class=\"logo\" src=\"https://adcdn.zplayads.com/assets/images/zplayads_logo.png\"/>\n        </div>\n\n      </div>\n    </div>\n    \n    <script src=\"https://adcdn.zplayads.com/engine/prod/3.0.0/atmos.min.js\"></script>\n    \n  </body>\n</html",
            "image_url": "",
            "w": 640,
            "h": 960,
            "app_bundle": "com.zplay.cn",
            "target_url": "http://www.zplay.cn",
            "click_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=42aff45315acb70d&t=1&bid_id=0bug6s1COrdw4rZwoY1AtZst4npvg3&ad_id=12345&type=0&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=YlPKWATzcV8O4PyFuQc7Kw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap64366690d9b306604610228a465db1aa97e42e89",
                "http://test.adx.yumimobi.com/page_click.php"
            ],
            "imp_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=699706254edd7d40&t=0&bid_id=0bug6s1COrdw4rZwoY1AtZst4npvg3&ad_id=12345&type=0&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=YlPKWATzcV8O4PyFuQc7Kw&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap64366690d9b306604610228a465db1aa97e42e89",
                "http://test.adx.yumimobi.com/page_show.php"
            ],
            "refresh_interval": 0,
            "inventory_type": 10,
            "ssp_id": "10",
            "logo_url":"http://static.zplay.cn/wap/img/ad/adlogo_yumi.png",
            "price": 0
        }
    ],
    "msg": "",
    "result": 0
}
```

### 插屏视频广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持视频广告，即包含3，且返回的广告中 `invenroy_type` 为3，则该广告为插屏的视频广告。该广告除了包含普通插屏支持的素材参数外，还包含video对象，用来设置播放视频的地址和监测等信息。
下面以插屏的图文元素为例：

```json
{
    "ads": [
        {
            "id": "12345",
            "place_id": "",
            "action": 2,
            "image_url": "http://ppgz.zplay.cn/image/adx_img/600-600.png",
            "w": 640,
            "h": 960,
            "app_bundle": "com.zplay.cn",
            "target_url": "http://www.zplay.cn",
            "click_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=1caadc2eca3cdf3a&t=1&bid_id=0bulZf1COwg645eaAm0q12Wl0KQyQc&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=Fp_KWHCqskhzQOB8UEukkQ&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dclick%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
                "http://test.adx.yumimobi.com/page_click.php"
            ],
            "imp_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=7d7b2ba2193af5f1&t=0&bid_id=0bulZf1COwg645eaAm0q12Wl0KQyQc&ad_id=12345&type=1&dsp_id=129&plmn=46001&ssp_id=1&app_id=1007716&app_bundle_id=com.zplay.classicpopstar&price_enc=Fp_KWHCqskhzQOB8UEukkQ&cur=CNY&u=http%3A%2F%2Ftest.adx.yumimobi.com%2Fmock.php%3Ftype%3Dimp%26id%3D123&adid_sha1=e9ace9d5e87035219a227db42b915909a91c989a&test=1&pid=zap417d768fb04d5db77bfc65af2a8ce736bc8122ae",
                "http://test.adx.yumimobi.com/page_show.php"
            ],
            "refresh_interval": 0,
            "inventory_type": 3,
            "title": "长腿爸爸",
            "desc": "一个非常好玩的亲子游戏，快来体验吧",
            "ssp_id": "10",
            "price": 0,
            "video": {
                "url": "http://download.ydstatic.com/sdk/mp4/my%20wife%20is%20student%20union%20president.mp4",
                "play_duration": 15,
                "player_start_trackers": [
                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=205&play_percent=0.0"
                ],
                "player_end_trackers": [
                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=205&play_percent=1.0"
                ]
            }
        }
    ],
    "msg": "",
    "result": 0
}
```

## 开屏

### 开屏请求示例

> 同banner、插屏广告一样，开屏广告在请求的时候也需要通过 `inventory_types` 标明支持的物料类型，通常也包含图片，图文，html三种类型的广告，与插屏广告不同的是，请求参数中ad_type为2，是在应用刚开始启动的时候展示，具体展示示例可参考插屏的三种广告返回和展示示例。

```json

	{
	    "ver": "1.1",
	    "ssp_token": "zplay提供的ssp_token",
	    "need_https": 0,
	    "app": {
	        "id": "zplay提供的app_id",
	        "name": "DrivingTest",
	        "app_key": "zplay提供的app_key",
	        "bundle": "cn.eclicks.drivingtest",
	        "ver": "",
	        "cat": []
	    },
	    "device": {
	        "model": "vivoX7",
	        "brand": "vivo",
	        "adt": 1,
	        "connection_type": "wifi",
	        "carrier": 0,
	        "orientation": 1,
	        "mac": "20:5d:47:0b:33:38",
	        "imei": "862505031462331",
	        "android_id": "840be0b0d00e6169",
	        "openudid": "e4791d89-dda9-36c0-b9df-edacc24b01c8",
	        "os_type": "android",
	        "os_version": "5.1.1",
	        "screen": {
	            "w": 1080,
	            "h": 1920,
	            "dpi": 480
	        },
	        "geo": {
	            "lat": 31.151308,
	            "lon": 108.36747
	        }
	    },
	    "ads": [
	        {
	            "type": 2,
	            "place_id": "50otuc9h",
	            "floor_price": 100,
	            "currency": "CNY",
	            "w": 720,
	            "h": 1038,
	            "inventory_types": [
	                1,
	                2,
	                4,
	                5
	            ]
	        }
	    ]
	}
```

### 开屏图片广告返回示例

> 参考banner图片广告，展示返回广告中的 `img_url` 图片即可。

### 开屏图文广告返回示例

> 参考插屏的图文广告返回示例，需要返回内容中的 `img_url` `title` `desc` 组合拼装展示。

### 开屏html广告返回示例

> 参考banner html广告返回示例即可，将返回的 `html_snippet` 中的html代码在app中展示出来即可。


## 原生广告

### 原生广告请求示例

> `ad_type` 为 `3` ，`invenroty_types` 为 `[6]` 请求的元素为媒体根据自己展示需要定义的元素块

```json

	{
	    "ver": "1.1",
	    "ssp_token": "zplay提供的ssp_token",
	    "app": {
	        "id": "zplay提供的app_id",
	        "name": "app name",
	        "app_key": "zplay提供的app_key",
	        "bundle": "bundle.com"
	    },
	    "device": {
	        "model": "iPhone 5 (A1429/A1442)",
	        "make": "Apple",
	        "brand": "Apple",
	        "ip": "223.74.73.17",
	        "connection_type": "wifi",
	        "carrier": 0,
	        "os_version": "10.2.1",
	        "os_type": "ios",
	        "mac": null,
	        "openudid": "983ADE10-20E6-441E-9078-2FA932787E67",
	        "ios_adid": "983ADE10-20E6-441E-9078-2FA932787E67"
	    },
	    "ads": [
	        {
	            "inventory_types": [
	                6
	            ],
	            "type": 3,
	            "place_id": "gk8cmfh8",
	            "floor_price": 0,
	            "native": {
	                "layout": 3,
	                "assets": [
	                    {
	                        "id": 0,
	                        "title": {
	                            "len": 30
	                        }
	                    },
	                    {
	                        "id": 2,
	                        "img": {
	                            "type": 3,
	                            "w": 640,
	                            "h": 320
	                        }
	                    }
	                ]
	            },
	            "w": 640,
	            "h": 320
	        }
	    ]
	}
```

### 原生广告返回示例

```json

	{
	    "Ad_Responses": [
	        {
	            "id": "611",
	            "place_id": "",
	            "action": 2,
	            "image_url": "",
	            "w": 640,
	            "h": 320,
	            "target_url": "",
	            "click_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=28dcac6e3119e34c&t=1&bid_id=0bts0K1COxc026JViX3879I314lTQu&ad_id=611&type=3&dsp_id=20&plmn=46000&ssp_id=445&app_id=1007816&app_bundle_id=com.idol.ios&price_enc=HK3KWH-GwiN5V-nX4DdXDQ&cur=CNY&adid_sha1=5a126d40d994ef41d3e747339fe64bb0e0091b37&pid=zap60bb78bc056d737fd90773832834930d264cc5fd",
	                "http://c.gdt.qq.com/gdt_mclick.fcg?viewid=NtupfjoJRlZpXS_vNhoQmyx9s9fY8vM3mHxNC26zSmAHJ_IlOArCMMTcfB_9T07!DMyJmd5Qu43LRxKoflPKo4F6r3Bzww5DQwPhwcHhVhnRQnVe19Ik2rN9EES5JCqJL1FtWzL3BB6hXW3!92M!965AKLz3UEZbCHUy08zSwJXSbf!FQ7Oc60FaHmLg!N4pwI9AqxQCYMTHeICIhhXMcw&jtype=0&i=1&os=1?viewid=NtupfjoJRlZpXS_vNhoQmyx9s9fY8vM3mHxNC26zSmAHJ_IlOArCMMTcfB_9T07!DMyJmd5Qu43LRxKoflPKo4F6r3Bzww5DQwPhwcHhVhnRQnVe19Ik2rN9EES5JCqJL1FtWzL3BB6hXW3!92M!965AKLz3UEZbCHUy08zSwJXSbf!FQ7Oc60FaHmLg!N4pwI9AqxQCYMTHeICIhhXMcw&acttype=0&s=%7B%22down_x%22%3A0%2C%22down_y%22%3A0%7D"
	            ],
	            "imp_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=762b36d6447913fd&t=0&bid_id=0bts0K1COxc026JViX3879I314lTQu&ad_id=611&type=3&dsp_id=20&plmn=46000&ssp_id=445&app_id=1007816&app_bundle_id=com.idol.ios&price_enc=HK3KWH-GwiN5V-nX4DdXDQ&cur=CNY&adid_sha1=5a126d40d994ef41d3e747339fe64bb0e0091b37&pid=zap60bb78bc056d737fd90773832834930d264cc5fd",
	                "http://v.gdt.qq.com/gdt_stats.fcg?count=1&viewid0=NtupfjoJRlZpXS_vNhoQmyx9s9fY8vM3mHxNC26zSmAHJ_IlOArCMMTcfB_9T07!DMyJmd5Qu43LRxKoflPKo4F6r3Bzww5DQwPhwcHhVhnRQnVe19Ik2rN9EES5JCqJL1FtWzL3BB6hXW3!92M!965AKLz3UEZbCHUy08zSwJXSbf!FQ7Oc60FaHmLg!N4pwI9AqxQCYMTHeICIhhXMcw"
	            ],
	            "refresh_interval": 0,
	            "inventory_type": 6,
	            "ssp_id": "9",
	            "ex_param": [
	                "",
	                "",
	                "",
	                "",
	                ""
	            ],
	            "native": {
	                "assets": [
	                    {
	                        "id": 0,
	                        "title": {
	                            "text": "饿了么"
	                        }
	                    },
	                    {
	                        "id": 2,
	                        "img": {
	                            "url": "http://pgdt.gtimg.cn/gdt/0/DAALNssAUAALQABaBYqlw-BwDr80Wr.jpg/0?ck=f267de6cc4dbe0c2ba357d3233566692",
	                            "w": 640,
	                            "h": 320
	                        }
	                    }
	                ],
	                "link": {
	                    "url": "http://c.gdt.qq.com/gdt_mclick.fcg?viewid=NtupfjoJRlZpXS_vNhoQmyx9s9fY8vM3mHxNC26zSmAHJ_IlOArCMMTcfB_9T07!DMyJmd5Qu43LRxKoflPKo4F6r3Bzww5DQwPhwcHhVhnRQnVe19Ik2rN9EES5JCqJL1FtWzL3BB6hXW3!92M!965AKLz3UEZbCHUy08zSwJXSbf!FQ7Oc60FaHmLg!N4pwI9AqxQCYMTHeICIhhXMcw&jtype=0&i=1&os=1",
	                    "type": 2
	                }
	            },
	            "zplay": {
	                "app_id": "1105857971",
	                "position_sid": "5000214883692309"
	            },
	            "price": 0
	        }
	    ],
	    "msg": "",
	    "result": 0
	}
```

## 视频广告

### 视频广告请求示例

> 视频请求的ad_type为4，inventory_types 为 [3]

```json

	{
	    "ads": [
	        {
	            "place_id": "sdbds23sd",
	            "floor_price": 100,
	            "currency": "CNY",
	            "h": 960,
	            "inventory_types": [
	                3
	            ],
	            "place_id": "FPA52248",
	            "pos": 0,
	            "type": 4,
	            "w": 640
	        }
	    ],
	    "ad": {},
	    "app": {
	        "app_key": "zplay提供的app_key",
	        "bundle": "",
	        "id": "zplay提供的app_id",
	        "name": "app name",
	        "ver": "5.0.0"
	    },
	    "device": {
	        "adt": 1,
	        "android_id": "bdd66b6d38c69335",
	        "carrier": 0,
	        "connection_type": "wifi",
	        "geo": {
	            "accu": 0,
	            "lat": 0,
	            "lon": 0
	        },
	        "imei": "861619032588944",
	        "ios_adid": "",
	        "local": "",
	        "mac": "26:28:46:09:1d:4f",
	        "make": "samsung",
	        "model": "SM-T810",
	        "orientation": 1,
	        "os_type": "android",
	        "os_version": "6.0",
	        "plmn": "",
	        "screen": {
	            "dpi": 240,
	            "h": 1536,
	            "w": 1152
	        }
	    },
	    "is_tail": 0,
	    "is_test": 0,
	    "sdk_ver": "androidmedia1.2.1.2",
	    "ssp_token": "10000",
	    "user": {
	        "age": 0,
	        "gender": 0
	    },
	    "ver": "1.1"
	}
```

### 视频广告返回示例

```json

	{
	    "Ad_Responses": [
	        {
	            "id": "19046454",
	            "place_id": "",
	            "action": 6,
	            "image_url": "http://oimageb1.ydstatic.com/image?id=-3419818951519079008&product=adpublish",
	            "w": 640,
	            "h": 960,
	            "target_url": "http://dl.hdslb.com/mobile/latest/iBiliPlayer-youdao010.apk",
	            "click_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=6dc86f24a6f5c527&t=1&bid_id=0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U&ad_id=19046454&type=4&dsp_id=602&plmn=46000&ssp_id=1&app_id=1000481&app_bundle_id=&price_enc=G63KWEiAWBhhBc34J0nXRw&cur=CNY&u=http%3A%2F%2Fp.clkservice.youdao.com%2Fclk%2Frequest.s%3Fk%3D4nx6iXFBcrUkfq9Pk%252BQJmS9cBWcnVn%252FvkeOOR6zbRfHXxo%252BoRxcJpjjAgKuViCqv52rawaCcQI2R6UiK1fhynWLAHXSMp8aBaL0cKcYl8mtcrJiEXwf%252FhYZwCCBIYpYkWLSHlAnWvRC13XK2RLk2jd4D4lkCrc2ittfTajZlNcoefJW0XPAIqdeMIrNGkCZe%252FIFW0I4LteiV%252FrsRj%252F2xlLTp7UV9cZRJUk2Sey94ryegaXlA2SmQ3dJfV6xO2oCdMS8f%252B01OZiTuuiQtlRc%252BWkrC%252B5WXQRtCToR922rjacEjo3fGWc4cm6wN1jOsjZSEH%252F0qWLM832XuHVN3JUQ9DTIdG%252Bczoz1jkVv%252BJLo0%252FZwEOrMBmh5izfkJarUODPOoSGB0t8xtHvnNANy3ZHFPxJCTW0wUjwoO7K%252B9UkSbSq%252FkjTG%252BKdoF6%252BhjZrJzw2TteqAopSl%252FYsVWeCn9yHMoUR8j1x3%252F9Hr3%252BIHmehpO3ELBqJMgONppinYjWbikMXTzWqtaMUWFLz9almr9ZUdRE97S5kFykRuSF4oJ2i6ksee7MphQ06%252BNvts2J95dRFtV3YUlk9fgA%252BpfBEtQqOc2X8sfmQxG3vA7UWSzhtHd8BIh%252FdSdWeVZvjrWauuguVd4JOR5t8aXQKklWTtBewgdWvBWbyhZFXFWzCkoig9r3VLN8ayV3syYFo%252FG5P6LpNmQ%252FCu1PDzVlTvQ2FsbzgKBELr5rXlh5BMbIp282bQgB6nphmiWxo0B0FCOyQybgIsX6mleh6fw0t8WAp34OCu1vpCvw5E%252FS15%252BHM8wThy7PuzXxo%252BoRxcJpjjAgKuViCqv18aPqEcXCaY4wICrlYgqrx7cJrWwEnlELPOipPDadCLw6dP9Tw26XG5BNsUzi2UI%26isrd%3D0%26youdao_bid%3D0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U%26youdao_deviceId%3Db064bbe4e5749412f7770bc1c0d8663999c8bd1f&adid_sha1=&aid_sha1=b064bbe4e5749412f7770bc1c0d8663999c8bd1f&pid=FPA52248"
	            ],
	            "imp_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=7f95f85bc960d054&t=0&bid_id=0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U&ad_id=19046454&type=4&dsp_id=602&plmn=46000&ssp_id=1&app_id=1000481&app_bundle_id=&price_enc=G63KWEiAWBhhBc34J0nXRw&cur=CNY&u=http%3A%2F%2Fdsp-impr2.youdao.com%2Fz.gif%3Fyd_ewp%3DG63KWEiAWBhhBc34J0nXRw%26yd_ext%3DEnQKATESIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiIksItsCKCRDM-q8CGPTjKSDU1BEo8k4wDjgOZQCQXUVwAHgAgAEAmAEBogELVHJhZGl0aW9uYWy6ARJ7Ik9SREVSRURfSUQiOiIxIn0wAyIeMGJ0czBLMUNPeGJaMjVCVkxKNGFLT3N5M2xaSjlVKHQwADoAQgBSDjExOS4xMzEuMjIyLjgxag0xNDg5Njc3NTk1MjE5eACCAQCIAdkbkAHT5NC9rSuoAQGwAQG4AQHCAQQyNDI00AEB2gEoYjA2NGJiZTRlNTc0OTQxMmY3NzcwYmMxYzBkODY2Mzk5OWM4YmQxZuIBGRoAMhBiZGQ2NmI2ZDM4YzY5MzM1OgM2LjD6AQU1LjAuMA&adid_sha1=&aid_sha1=b064bbe4e5749412f7770bc1c0d8663999c8bd1f&pid=FPA52248"
	            ],
	            "refresh_interval": 0,
	            "inventory_type": 3,
	            "ssp_id": "10",
	            "video": {
	                "url": "http://download.ydstatic.com/sdk/mp4/my%20wife%20is%20student%20union%20president.mp4",
	                "play_duration": 15,
	                "player_start_trackers": [
	                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=205&play_percent=0.0"
	                ],
	                "player_end_trackers": [
	                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=205&play_percent=1.0"
	                ]
	            },
	            "price": 0
	        }
	    ],
	    "msg": "",
	    "result": 0
	}
```


### 视频可玩广告返回示例

> 如果媒体请求广告时，通过 `inventory_types` 标明支持可玩广告，即包含10，且返回的广告中 `invenroy_type` 为10，则该广告为视频的可玩广告。可玩广告是可以交互操作的html，并填充到html_snippet参数中。<font color="red">注意返回参数中不再有video对象</font>。

```json

	{
	    "Ad_Responses": [
	        {
	            "id": "19046454",
	            "place_id": "",
	            "action": 6,
	            "image_url": "http://oimageb1.ydstatic.com/image?id=-3419818951519079008&product=adpublish",
	            "w": 640,
	            "h": 960,
	            "target_url": "http://dl.hdslb.com/mobile/latest/iBiliPlayer-youdao010.apk",
	            "click_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=6dc86f24a6f5c527&t=1&bid_id=0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U&ad_id=19046454&type=4&dsp_id=602&plmn=46000&ssp_id=1&app_id=1000481&app_bundle_id=&price_enc=G63KWEiAWBhhBc34J0nXRw&cur=CNY&u=http%3A%2F%2Fp.clkservice.youdao.com%2Fclk%2Frequest.s%3Fk%3D4nx6iXFBcrUkfq9Pk%252BQJmS9cBWcnVn%252FvkeOOR6zbRfHXxo%252BoRxcJpjjAgKuViCqv52rawaCcQI2R6UiK1fhynWLAHXSMp8aBaL0cKcYl8mtcrJiEXwf%252FhYZwCCBIYpYkWLSHlAnWvRC13XK2RLk2jd4D4lkCrc2ittfTajZlNcoefJW0XPAIqdeMIrNGkCZe%252FIFW0I4LteiV%252FrsRj%252F2xlLTp7UV9cZRJUk2Sey94ryegaXlA2SmQ3dJfV6xO2oCdMS8f%252B01OZiTuuiQtlRc%252BWkrC%252B5WXQRtCToR922rjacEjo3fGWc4cm6wN1jOsjZSEH%252F0qWLM832XuHVN3JUQ9DTIdG%252Bczoz1jkVv%252BJLo0%252FZwEOrMBmh5izfkJarUODPOoSGB0t8xtHvnNANy3ZHFPxJCTW0wUjwoO7K%252B9UkSbSq%252FkjTG%252BKdoF6%252BhjZrJzw2TteqAopSl%252FYsVWeCn9yHMoUR8j1x3%252F9Hr3%252BIHmehpO3ELBqJMgONppinYjWbikMXTzWqtaMUWFLz9almr9ZUdRE97S5kFykRuSF4oJ2i6ksee7MphQ06%252BNvts2J95dRFtV3YUlk9fgA%252BpfBEtQqOc2X8sfmQxG3vA7UWSzhtHd8BIh%252FdSdWeVZvjrWauuguVd4JOR5t8aXQKklWTtBewgdWvBWbyhZFXFWzCkoig9r3VLN8ayV3syYFo%252FG5P6LpNmQ%252FCu1PDzVlTvQ2FsbzgKBELr5rXlh5BMbIp282bQgB6nphmiWxo0B0FCOyQybgIsX6mleh6fw0t8WAp34OCu1vpCvw5E%252FS15%252BHM8wThy7PuzXxo%252BoRxcJpjjAgKuViCqv18aPqEcXCaY4wICrlYgqrx7cJrWwEnlELPOipPDadCLw6dP9Tw26XG5BNsUzi2UI%26isrd%3D0%26youdao_bid%3D0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U%26youdao_deviceId%3Db064bbe4e5749412f7770bc1c0d8663999c8bd1f&adid_sha1=&aid_sha1=b064bbe4e5749412f7770bc1c0d8663999c8bd1f&pid=FPA52248"
	            ],
	            "imp_trackers": [
	                "http://stat.adx.yumimobi.com/api/s?r=7f95f85bc960d054&t=0&bid_id=0bts0K1COxbZ25BVLJ4aKOsy3lZJ9U&ad_id=19046454&type=4&dsp_id=602&plmn=46000&ssp_id=1&app_id=1000481&app_bundle_id=&price_enc=G63KWEiAWBhhBc34J0nXRw&cur=CNY&u=http%3A%2F%2Fdsp-impr2.youdao.com%2Fz.gif%3Fyd_ewp%3DG63KWEiAWBhhBc34J0nXRw%26yd_ext%3DEnQKATESIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiIksItsCKCRDM-q8CGPTjKSDU1BEo8k4wDjgOZQCQXUVwAHgAgAEAmAEBogELVHJhZGl0aW9uYWy6ARJ7Ik9SREVSRURfSUQiOiIxIn0wAyIeMGJ0czBLMUNPeGJaMjVCVkxKNGFLT3N5M2xaSjlVKHQwADoAQgBSDjExOS4xMzEuMjIyLjgxag0xNDg5Njc3NTk1MjE5eACCAQCIAdkbkAHT5NC9rSuoAQGwAQG4AQHCAQQyNDI00AEB2gEoYjA2NGJiZTRlNTc0OTQxMmY3NzcwYmMxYzBkODY2Mzk5OWM4YmQxZuIBGRoAMhBiZGQ2NmI2ZDM4YzY5MzM1OgM2LjD6AQU1LjAuMA&adid_sha1=&aid_sha1=b064bbe4e5749412f7770bc1c0d8663999c8bd1f&pid=FPA52248"
	            ],
	            "refresh_interval": 0,
	            "inventory_type": 10,
	            "ssp_id": "10",
	            "html_snippet":"<!DOCTYPE html>\n<html>\n  <head>\n    <meta name=\"viewport\" content=\"user-scalable=no, width=device-width, initial-scale=1, maximum-scale=1\">\n    <title>Atmosplayer</title>\n    <meta charset=\"utf-8\"/>\n    <script>\n      window.gestures = [\n  [\n    {\n      \"id\": 0,\n      \"type\": \"swipe\",\n      \"attack\": 1,\n      \"loopStart\": 551,\n      \"target\": 6651,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": true,\n      \"swipeDirection\": \"LEFT\",\n      \"loop\": true\n    }\n  ],\n  [\n    {\n      \"id\": 1,\n      \"type\": \"swipe\",\n      \"attack\": 9049,\n      \"loopStart\": 9499,\n      \"target\": 14449,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": true,\n      \"swipeDirection\": \"RIGHT\",\n      \"loop\": true\n    }\n  ],\n  [\n    {\n      \"id\": 2,\n      \"type\": \"swipe\",\n      \"attack\": 18060,\n      \"loopStart\": 18710,\n      \"target\": 23860,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": true,\n      \"swipeDirection\": \"UP\",\n      \"loop\": true\n    }\n  ],\n  [\n    {\n      \"id\": 3,\n      \"type\": \"swipe\",\n      \"attack\": 28738,\n      \"loopStart\": 30288,\n      \"target\": 35036,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": true,\n      \"swipeDirection\": \"DOWN\",\n      \"loop\": true\n    }\n  ],\n  [\n    {\n      \"id\": 4,\n      \"type\": \"tap\",\n      \"attack\": 38506,\n      \"target\": 40100,\n      \"fullscreen\": true,\n      \"shapes\": [\n        {\n          \"type\": \"circle\",\n          \"x\": 0.42328042328042326,\n          \"y\": 0.23809523809523808,\n          \"radius\": 0.08465608465608465\n        }\n      ],\n      \"mandatory\": false,\n      \"tapDirection\": 1,\n      \"tapCount\": 1\n    }\n  ]\n];\n      window.showUserGuide = false;\n      window.userGuideUrl = 'undefined';\n      window.userGuidePosition = {};\n      window.installAttributes = {\"x\":0.2779827900049644,\"y\":0.04047619047619048,\"width\":0.49487009763362566,\"percentage\":true};\n      window.showFloatingMenu = true;\n      window.videoOrientation = 0;\n      window.disableUserFeedback = false;\n\n      window.hasEndCard = false;\n      window.endCardSettings = undefined;\n      \n      \n    </script>\n  </head>\n  <body>\n    <div id=\"mainContainer\">\n      <img id=\"loadingImage\" src=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/load.jpg\" />\n      <div id=\"rotatedContainer\">\n\n        <img id=\"closeButton\" src=\"https://adcdn.zplayads.com/assets/images/x_button.png\"/>\n        <img id=\"restartButton\" src=\"https://adcdn.zplayads.com/assets/images/restart.png\"/>\n\n        <img id=\"installButton\" src=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/downloadImage.png?key=641\" />\n\n        <video id=\"atmosPlayer\" webkit-playsinline playsinline muted preload=\"auto\" src=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/transcoded_video_1500kbps.mp4\" poster=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/load.jpg\" autoplay></video>\n        <audio id=\"bgMusicPlayer\" src=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/bgMusic.mp3?key=284\" type=\"audio/mpeg\" loop></audio>\n\n        <video id=\"atmosPlayerEndCard\" webkit-playsinline playsinline muted preload=\"auto\" src=\"\" poster=\"https://adcdn.zplayads.com/assets/prod/63479990-3d68-11e8-a313-55140a049e95/load.jpg\" style=\"z-index: -10;\"></video>\n\n        <canvas id=\"gestureDetector\"></canvas>\n        <canvas id=\"userFeedback\"></canvas>\n\n        <div id=\"floatingMenu\" class=\"simple\">\n          <span class=\"title\">¿ÉÍæµÄÃÔÄãÓÎÏ·</span><img alt=\"gamebox\" class=\"logo\" src=\"https://adcdn.zplayads.com/assets/images/zplayads_logo.png\"/>\n        </div>\n\n      </div>\n    </div>\n    \n    <script src=\"https://adcdn.zplayads.com/engine/prod/3.0.0/atmos.min.js\"></script>\n    \n  </body>\n</html>",
	            "price": 0
	        }
	    ],
	    "msg": "",
	    "result": 0
	}
```
