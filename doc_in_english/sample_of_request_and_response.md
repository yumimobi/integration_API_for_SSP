# SAMPLE OF JSON'S REQUEST AND RESPONSE

- [SAMPLE OF JSON'S REQUEST AND RESPONSE](#sample-of-jsons-request-and-response)
  - [banner](#banner)
    - [request of banner](#request-of-banner)
    - [response using image of banner](#response-using-image-of-banner)
      - [snapshot of banner using image](#snapshot-of-banner-using-image)
    - [response of banner using image and text](#response-of-banner-using-image-and-text)
      - [snapshot of banner using image and text](#snapshot-of-banner-using-image-and-text)
    - [response of banner using html snippet](#response-of-banner-using-html-snippet)
      - [response using html snippet of banner](#response-using-html-snippet-of-banner)
  - [interstitial](#interstitial)
    - [request of interstitial](#request-of-interstitial)
    - [response using image of interstitial](#response-using-image-of-interstitial)
      - [snapshot using image of interstitial](#snapshot-using-image-of-interstitial)
    - [response using image and text of interstitial](#response-using-image-and-text-of-interstitial)
      - [snapshot using image and text of interstitial](#snapshot-using-image-and-text-of-interstitial)
    - [response using html snippet of interstitial](#response-using-html-snippet-of-interstitial)
    - [response using playable of interstitial](#response-using-playable-of-interstitial)
    - [response using video of interstitial](#response-using-video-of-interstitial)
  - [splash](#splash)
    - [request of splash ads](#request-of-splash-ads)
      - [snapshot using image of splash](#snapshot-using-image-of-splash)
    - [response using image and text of splash](#response-using-image-and-text-of-splash)
    - [response using html snippet of splash](#response-using-html-snippet-of-splash)
  - [native](#native)
    - [request of native ads](#request-of-native-ads)
    - [response of native ads](#response-of-native-ads)
  - [rewarded video](#rewarded-video)
    - [request of rewarded video](#request-of-rewarded-video)
    - [response of rewarded video](#response-of-rewarded-video)
    - [response of playable video](#response-of-playable-video)

> - you can use test token  in your testing so that you can view the result. please change to formal token and APP ID when you release the integration, or you will never get any revenue.

>  testing token is ``EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=`` 

> testing APP ID：

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

> - there are some main wrong values: -1：types of parameter is mistake; -3: no ad fill; -4: this traffic was banned; -5: failed to check parameters or parameters is invalid.

## banner

### request of banner

```json
{
  "ver": "1.1",
  "ssp_token": "EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=",
  "need_https": 0,
  "app": {
    "id": "bg76gil7",
    "name": "DrivingTest",
    "app_key": "app_key",
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
      "inventory_types": [1, 2, 4, 5]
    }
  ]
}
```

### response using image of banner

> if parameter `inventory_types:[]` includes `1(type of material is image)`,YUMI Adx wil return image ads and the parameter `inventory_types:[]` in response also is 1.

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
      "ex_param": ["", "", "", "", ""],
      "price": 0
    }
  ],
  "msg": "",
  "result": 0
}
```

#### snapshot of banner using image

![banner](/img/banner_img1.jpg)

### response of banner using image and text

> if parameter `inventory_types:[]` includes `2(type of material is image and text)`, YUMI Adx will return image and text ads, and the parameter `inventory_type` in response also is `2`, besides, parameters title and desc in response will be filled in.

jump：

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

android download：

```json
{
    "ads": [
        {
            "id": "464",
            "place_id": "",
            "action": 6,
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
            "app_download_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=607f65d9268021d3&t=2&bid_id=0bts0K1CObXU1MkqKd28U76h45LrcY&ad_id=464&type=2&dsp_id=20&plmn=46000&ssp_id=449&app_id=1007877&app_bundle_id=cn.eclicks.drivingtest&price_enc=Xm7JWFA9pOhXsloDA1CMNw&cur=CNY&u=http%3A%2F%2Fv.gdt.qq.com%2Fgdt_stats.fcg%3Fcount%3D1%26viewid0%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg&adid_sha1=&aid_sha1=67d3bc8ba4a697f34c7165779438873896665f3e&pid=zap937e286143f6d462185316171ff574a7b10077f6"
            ],
            "app_download_finish_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=607f65d9268021d3&t=3&bid_id=0bts0K1CObXU1MkqKd28U76h45LrcY&ad_id=464&type=2&dsp_id=20&plmn=46000&ssp_id=449&app_id=1007877&app_bundle_id=cn.eclicks.drivingtest&price_enc=Xm7JWFA9pOhXsloDA1CMNw&cur=CNY&u=http%3A%2F%2Fv.gdt.qq.com%2Fgdt_stats.fcg%3Fcount%3D1%26viewid0%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg&adid_sha1=&aid_sha1=67d3bc8ba4a697f34c7165779438873896665f3e&pid=zap937e286143f6d462185316171ff574a7b10077f6"
            ],
            "app_activate_trackers": [
                "http://stat.adx.yumimobi.com/api/s?r=607f65d9268021d3&t=4&bid_id=0bts0K1CObXU1MkqKd28U76h45LrcY&ad_id=464&type=2&dsp_id=20&plmn=46000&ssp_id=449&app_id=1007877&app_bundle_id=cn.eclicks.drivingtest&price_enc=Xm7JWFA9pOhXsloDA1CMNw&cur=CNY&u=http%3A%2F%2Fv.gdt.qq.com%2Fgdt_stats.fcg%3Fcount%3D1%26viewid0%3Dt6o7__bYZoWql51I7krTHXw7wX3HwUO9FjIJt6rPb8mySO4Cu%21%21XqJrUNtcEUqqnhweRJ4LLS2m49e8HowA62q%219A3lx4Doz_9tzhiFUUlCMXWdN2EKozjMRBb1KLFPtzKPDguyL1XXhtJIXEQlUJVWUlBGubb1_%21csNQ1sjv6cL2Bv2x6hgcGzZKiqUH1N1juj87SFLvPyB2QAPdV57Lg&adid_sha1=&aid_sha1=67d3bc8ba4a697f34c7165779438873896665f3e&pid=zap937e286143f6d462185316171ff574a7b10077f6"
            ],
            "refresh_interval": 90,
            "inventory_type": 1,
            "ssp_id": "9",
            "download_file_name": "test_download_appname",
            "file_size": 1024,
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

#### snapshot of banner using image and text

![test2](/img/banner-pic-test2.jpg)

### response of banner using html snippet

> if parameter `inventory_types:[]` includes `4(type of material is html snippet)`, YUMI Adx will return html snippet ads, and the parameter `inventory_type` in response also is `4`.

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

> SSP should render ads directly using the content of `html_snippet` when the value of `invenroy[]` in response is 4.

#### response using html snippet of banner

![banner_html](/img/banner_html_ad.PNG)

## interstitial

### request of interstitial

> interstitial ads also needs indicate the types of material through `inventory_types` parameter, it's similar with banner ads.

```json
{
  "ver": "1.1",
  "ssp_token": "EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=",
  "need_https": 0,
  "app": {
    "id": "bg76gil7",
    "name": "DrivingTest",
    "app_key": "app_key",
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
      "inventory_types": [1, 2, 4, 5]
    }
  ]
}
```

### response using image of interstitial

> its logic is similar with banner ads.

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

#### snapshot using image of interstitial

![interstitial_picture](/img/intersitial_pic_1.PNG)

### response using image and text of interstitial

> its logic is similar with banner ads.

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
      "title": "long leg dad",
      "desc": "a very fun game",
      "ssp_id": "10",
      "price": 0
    }
  ],
  "msg": "",
  "result": 0
}
```

### snapshot using image and text of interstitial

![interstitial_pic_text](/img/intersitial_pic_text.PNG)

### response using html snippet of interstitial

> if the parameter `inventory_types` includes 4, YUMI Adx will return the interstitial ads using http snippet.

### response using playable of interstitial

> If request parameter `inventory_types` includes 10(material type: Playable Ads), it indicates a publisher supports Playable ads. Meanwhile YUMI Mobi return parameter `inventory_type` will be 10. Playable ad is a kind of interactive manipulation html, ads materials will be filled in html_snippet parameter.

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

### response using video of interstitial

> If request parameter `inventory_types` includes 3(material type: Video), it indicates a publisher supports Interstitial Video ads. Meanwhile YUMI Mobi return parameter `inventory_type` will be 3. Except the general interstitial material parameter, Interstitial Video Ads contains a video object to set video url and monitoring info.

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
            "title": "test title",
            "desc": "test desc",
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

## splash

### request of splash ads

> interstitial ads also needs indicate the types of material through `inventory_types` parameter, it's similar with banner ads.

```json
{
  "ver": "1.1",
  "ssp_token": "EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=",
  "need_https": 0,
  "app": {
    "id": "bg76gil7",
    "name": "DrivingTest",
    "app_key": "app_key",
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
      "inventory_types": [1, 2, 4, 5]
    }
  ]
}
```

### snapshot using image of splash

> refer to [snapshot using image of banner](#snapshot-of-banner-using-image)

### response using image and text of splash

> refer to response using image and text of banner.

### response using html snippet of splash

> refer to response using html snippet of banner.

## native

### request of native ads

> if in the request, parameter `ad_type` is `3` and `invenroty_types` is `[6]`, this means YUMI Adx will return a native ads.

```json
{
  "ver": "1.1",
  "ssp_token": "EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=",
  "app": {
    "id": "yywtptfq",
    "name": "app name",
    "app_key": "app_key",
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
      "place_id": "gk8cmfh8",
      "inventory_types": [6],
      "type": 3,
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

### response of native ads

```json
{
  "ads": [
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
      "ex_param": ["", "", "", "", ""],
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

## rewarded video

### request of rewarded video

> it means YUMI Adx will return a video ads if the parameter `视频请求的`ad_type`is`4`and`inventory_types`is`[3]` in request.

```json
{
  "ads": [
    {
      "place_id": "dsdibu5j",
      "floor_price": 100,
      "currency": "CNY",
      "h": 960,
      "inventory_types": [3],
      "place_id": "FPA52248",
      "pos": 0,
      "type": 4,
      "w": 640
    }
  ],
  "ad": {},
  "app": {
    "app_key": "app_key",
    "bundle": "",
    "id": "bg76gil7",
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
  "ssp_token": "EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=",
  "user": {
    "age": 0,
    "gender": 0
  },
  "ver": "1.1"
}
```

### response of rewarded video

```json
{
    "ads": [
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
                ],
                "player_close_trackers": [
                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=206"
                ],
                "player_continue_trackers": [
                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=207"
                ],
                "player_restart_trackers": [
                    "http://dsp-impr2.youdao.com/impplay.s?ext=Ch4wYnRzMEsxQ094YloyNUJWTEo0YUtPc3kzbFpKOVUQ1NQRGPTjKSDM%2Bq8CKLbAigkwdDoOMTE5LjEzMS4yMjIuODFA0%2BTQva0rSAFSBDI0MjRaIDQxY2NjNmJmMjExMDhjZGRiZjZmYjJjNmU5ZmIzOTZiYihiMDY0YmJlNGU1NzQ5NDEyZjc3NzBiYzFjMGQ4NjYzOTk5YzhiZDFmeACCARBiZGQ2NmI2ZDM4YzY5MzM1igEAkAELmAGNAaIBBFdJRknCASQ0ZTYyNzIxYi03ZWM1LTRhMTYtOWNlYi1kMDVhNzkyYjUyNWTSAQU1LjAuMNoBAzYuMA%3D%3D&event_type=208&play_percent=0.0"
                ]
            },
            "price": 0
        }
    ],
    "msg": "",
    "result": 0
}
```


### response of playable video

> If request parameter `inventory_types` includes 10(material type: Playable Ads), it indicates a publisher supports Playable ads. Meanwhile YUMI Mobi return parameter `inventory_type`s` will be 10. Playable ad is a kind of interactive manipulation html, ads materials will be filled in html_snippet parameter. <font color="red">Please note return parameter will not contain a video object</font>.

```json

	{
	    "ads": [
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
