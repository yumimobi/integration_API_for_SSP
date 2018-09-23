# 文档更新记录

| 版本 | 作者 | 时间       | 备注                                                                                     |
| ---- | ---- | ---------- | ---------------------------------------------------------------------------------------- |
| v0.1 | Cui  | 2015.10.26 | 创建                                                                                     |
| v0.2 | Cui  | 2016.01.04 | 加入了针对自有ssp需求的一些字段                                                          |
| v0.3 | Cui  | 2016.07.18 | Request添加了Site对象，App对象添加了publisher对象                                        |
| v1.1 | Cui  | 2016.08.08 | Request添加Ads对象数组，支持一次请求多个广告位                                           |
| v2.0 | Cui  | 2016.12.01 | 添加need_https                                                                           |
| v2.1 | Cui  | 2016.12.07 | 修改Site对象为非必填；修复inventory_type的描述；修复原生required默认项描述               |
| v2.2 | Cui  | 2017.02.14 | 修复response.msg字段类型为string；更改floor_price为非必填项                              |
| V2.3 | Zhen | 2017.03.14 | 升级app.bundle、device.carrier、device.imei、device.ios_adid、screen.w、screen.h为必填项 |
| V2.4 | Zhen | 2017.04.01 | 修复在设备型号（model）、设备上的本地首选项 (local)这两个值在更新过程中的字段错误        |
| v2.5 | Zhen | 2017.04.07 | 为保证屏幕必填修改screen对象为必填项                                                     |
| v2.6 | Zhen | 2017.07.13 | 在response的Ad对象中添加logo_url                                                         |
| v2.7 | Zhen | 2017.12.28 | 增加对媒体替换点击点击坐标宏的要求                                                       |
| v2.8 | Zhen | 2018.03.14 | 修改is_test、is_tail描述，补充app_id、place_id替换为ADX标示的说明                        |
| v2.9 | niu  | 2018.09.10 | 修改部分接口及描述                                                                       |