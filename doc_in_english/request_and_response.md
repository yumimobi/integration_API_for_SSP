# API OF INTEGRATION

- [API OF INTEGRATION](#api-of-integration)
  - [introduction of document](#introduction-of-document)
  - [Preparation before integration](#preparation-before-integration)
  - [steps of request/response](#steps-of-requestresponse)
  - [instruction](#instruction)
    - [URL of request](#url-of-request)
    - [Communication Mode and Encoding](#communication-mode-and-encoding)
    - [request header](#request-header)
    - [request](#request)
      - [Request field](#request-field)
        - [app information](#app-information)
        - [website information](#website-information)
          - [Publisher information](#publisher-information)
        - [Device information](#device-information)
          - [Screen information](#screen-information)
          - [Geo information](#geo-information)
        - [User information](#user-information)
        - [Ad information](#ad-information)
          - [Native information](#native-information)
        - [Zplay information](#zplay-information)
    - [response](#response)
      - [Response field](#response-field)
        - [Ad information](#ad-information-1)
          - [Video information](#video-information)
        - [Zplay information](#zplay-information-1)
          - [Native information](#native-information-1)
    - [Report click-macro information](#report-click-macro-information)

## introduction of document

this document shows how developer(SSP, supply-side platform) integrate with YUMI Adx.

## Preparation before integration

please get the developer account info and token through asking for YUMI Adx account manager.

## steps of request/response

There are three steps in RTB processing:

1. User visits the site or APP that developer owns or serve for and make a ad request

2. Developer send the request to YUMI Adx

3. YUMI Adx reply developer Response

4. developer renders the ads according specification of this document

## instruction

### URL of request

When there is need to request ad, send a HTTP POST to the following address:
`bid.adx.yumimobi.com/adx`

### Communication Mode and Encoding

The underlying communication protocol between ZPLAY Ads ADX and SSP is HTTP, POST method, data using JSON format, UTF-8 encoding.

### request header

| http herder information | instruction                                                                                                                                                                                                                                 |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| X-Forwarded-For         | Include the real request address of the client, e.g. “8.8.8.8”. If integrated via server, please pass client address because server address will be blocked and regarded as fraud.                                                          |
| User-Agent              | User Agent of mobile device, e.g. “Mozilla/5.0 (iPad; CPU OS 5_0 like Mac OS X) AppleWebKit/534.46 (KHTML, like Gecko) Version/5.1 Mobile/9A334 Safari/7534.48.3”. Non-real User-Agent from server will be regarded as problematic traffic. |

### request

The Ad Request is a request sent by the SSP to the YUMI Ads ADX to call for an ad, via the Request URL noted above.

#### Request field

| parameter       | type             | mandatory | description                                                                                                                                                                                           |
| --------------- | ---------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ver             | string           | yes       | Protocol version, current version is 1.1                                                                                                                                                              |
| ssp_token       | string           | yes       | SSP token, offered by YUMI Adx account manager                                                                                                                                                        |
| is_test         | int              | no        | abandoned                                                                                                                                                                                             |
| is_tail         | int              | no        | abandoned                                                                                                                                                                                             |
| need_https      | int              | no        | for material's link or tracking url link, whether the prefix is https. 0 as default. 0: don’t need https, 1: need https for all materials and links.                                                  |
| sdk_ver         | string           | no        | sdk version, is only used for YUMI internal platform                                                                                                                                                  |
| app             | object           | yes       | app information                                                                                                                                                                                       |
| site            | object           | no        | site information                                                                                                                                                                                      |
| device          | object           | yes       | device information                                                                                                                                                                                    |
| user            | object           | no        | user information                                                                                                                                                                                      |
| ad              | object           | no        | ad information, apply to protocol version 1.0 and before, using `ads` from protocol version 1.1 and after.                                                                                            |
| ads             | array of objects | yes       | Ad information array                                                                                                                                                                                  |
| zplay           | object           | no        | is only used for YUMI internal platform                                                                                                                                                               |
| fallback_url    | string           | no        | jumping url that when arousing app failed                                                |
| fallback_action | int              | no        | action type of fallback_url, 1: open the fallback_url within WebView in-app, 2: open the fallback_url within system browser, 3: open map, 4: open dial, 5: play video, 6: download App, 7: arouse App |

##### app information

| parameter | type     | mandatory | description                                                                                                                                                  |
| --------- | -------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| id        | string   | yes       | Application ID, generated by YUMI Adx, such as "z0000001" or "iq3nktkh" after you registered the app on [https://www.yumimobi.com](https://www.yumimobi.com) |
| name      | string   | yes       | app name                                                                                                                                                     |
| app_key   | string   | no        | application key, this parameter have been abandoned.                                                                                                         |
| bundle    | string   | yes       | package name or bundle ID, such as "com.zplay.demo"                                                                                                          |
| ver       | string   | no        | application version                                                                                                                                          |
| cat       | []string | no        | application category                                                                                                                                         |
| publisher | object   | no        | publisher information                                                                                                                                        |

##### website information

| parameter  | type     | mandatory | description                                                                                                                                               |
| ---------- | -------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id         | string   | yes       | website ID, generated by YUMI Adx, such as "z0000001" or "iq3nktkh" after you registered the site on [https://www.yumimobi.com](https://www.yumimobi.com) |
| name       | string   | no        | website name                                                                                                                                              |
| domain     | string   | no        | website domain                                                                                                                                            |
| page       | string   | yes       | current page URL                                                                                                                                          |
| cat        | []string | no        | website category                                                                                                                                          |
| sectioncat | []string | no        | current channel category                                                                                                                                  |
| pagecat    | []string | no        | current page category                                                                                                                                     |
| ref        | string   | no        | Referrer URL                                                                                                                                              |
| search     | string   | no        | search keyword that goto current page                                                                                                                     |
| mobile     | int      | yes       | whether is a mobile page, If it’s mobile website, 1 indicates yes                                                                                         |
| keywords   | string   | no        | keywords of current page separated by ","                                                                                                                 |
| publisher  | object   | no        | publisher information                                                                                                                                     |

###### Publisher information

| parameter | type   | mandatory | description                |
| --------- | ------ | --------- | -------------------------- |
| name      | string | yes       | Publisher name             |
| domain    | string | no        | Publisher top level domain |
| cat       | string | no        | Publisher category         |

##### Device information

| parameter       | type    | mandatory | description                                                                                                                                                                                                                                                                                                                                                                     |
| --------------- | ------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| model           | string  | yes       | device model                                                                                                                                                                                                                                                                                                                                                                    |
| make            | string  | yes       | manufacturer, e.g. “Samsung”                                                                                                                                                                                                                                                                                                                                                    |
| brand           | string  | no        | cell brand, e.g. “MI4”                                                                                                                                                                                                                                                                                                                                                          |
| plmn            | string  | no        | public land mobile network (PLMN), as defined in telecommunications regulation, is a network that is established and operated by an administration or by a recognized operating agency (ROA) for the specific purpose of providing land mobile telecommunications services to the public, such as "46000"                                                                       |
| adt             | int | no        | If it’s allowed to target users by tracking user behavior, 0:not allowed, 1:allowed, default is 1                                                                                                                                                                                                                                                                               |
| connection_type | string  | yes       | Connection type, empty means unknown, wifi, 2g, 3g, 4g, ethernet, cell_unknown                                                                                                                                                                                                                                                                                                  |
| carrier         | int     | yes       | Carrier, 0:China Mobile, 1:Telecom, 3:Unicom, 4:unknown                                                                                                                                                                                                                                                                                                                         |
| orientation     | int     | yes       | Device orientation, 1:portrait, 3:landscape                                                                                                                                                                                                                                                                                                                                     |
| mac             | string  | no        | media access control address, is a unique identifier assigned to a network interface controller (NIC) for communications at the data link layer of a network segment. MAC addresses are used as a network address for most IEEE 802 network technologies, including Ethernet and Wi-Fi. In this context, MAC addresses are used in the medium access control protocol sublayer. |
| imei            | string  | no        | International Mobile Equipment Identity, is a number, usually unique, to identify 3GPP and iDEN mobile phones, as well as some satellite phones. (sending meid(mobile equipment identifier) if the mobile is CDMA2000)                                                                                                                                                          |
| imsi            | string  | no        | international mobile subscriber identity, is used to identify the user of a cellular network and is a unique identification associated with all cellular networks                                                                                                                                                                                                               |
| android_id      | string  | no        | Android ID is an unique ID to each device. It is used to identify your device for market downloads                                                                                                                                                                                                                                                                              |
| android_adid    | string  | no        | AAID(Google Advertising ID)                                                                                                                                                                                                                                                                                                                                                     |
| ios_adid        | string  | yes       | IDFA( Identifier for Advertising)                                                                                                                                                                                                                                                                                                                                               |
| idfv            | string  | no        | identifierForVendor, please view [more info](https://developer.apple.com/documentation/uikit/uidevice/1620059-identifierforvendor)                                                                                                                                                                                                                                              |
| openudid        | string  | no        | Openudid                                                                                                                                                                                                                                                                                                                                                                        |
| local           | string  | no        | Device language                                                                                                                                                                                                                                                                                                                                                                 |
| os_type         | string  | yes       | Operation system, "ios", "android", "wp"(windows phone)                                                                                                                                                                                                                                                                                                                         |
| os_version      | string  | yes       | Operation system version                                                                                                                                                                                                                                                                                                                                                        |
| screen          | object  | yes       | Screen info                                                                                                                                                                                                                                                                                                                                                                     |
| geo             | object  | no        | Geo info                                                                                                                                                                                                                                                                                                                                                                        |

###### Screen information

| parameter | type  | mandatory | description                                                                    |
| --------- | ----- | --------- | ------------------------------------------------------------------------------ |
| w         | int   | yes       | Landscape resolution, unit:pixel. If not passed, fill rate will be affected.   |
| h         | int   | yes       | Portrait resolution, unit:pixel. If not passed, fill rate will be affected.    |
| dpi       | int   | no        | Pixel density, unit:pixel numbers per inch                                     |
| pxratio   | float | no        | Physical pixel density, e.g. 1 on iPhone 3, 2 on iPhone 4, 3 on iPhone 6s Plus |

###### Geo information

| parameter | type  | mandatory | 描述                                                                                     |
| --------- | ----- | --------- | ---------------------------------------------------------------------------------------- |
| lat       | float | yes       | Latitude                                                                                 |
| lon       | float | yes       | longitude                                                                                |
| accu      | int   | no        | accurate, for reference [Decimal degrees](https://en.wikipedia.org/wiki/Decimal_degrees) |

##### User information

| parameter | type   | mandatory | description                                  |
| --------- | ------ | --------- | -------------------------------------------- |
| id        | string | no        | user id                                      |
| gender    | int    | no        | Gender, 0:female, 1:male, 2:other, 3:unknown |
| age       | int    | no        | age                                          |
| keywords  | array  | no        | keywords of user interest                    |
| ext       | UserExt object   |  no  | extended object |

#### UserExt information

| parameter | type | mandatory | description |
| ------- | ---- | ----| ----|
| consent | string | no | Whether or not to agree with the restriction of GDP R rule, this parameter value is not strictly in accordance with the IAB specification, `yes: agree, no: disagree`, not set, the default value is `yes` |

#### Regs information

| parameter | type | mandatory | description |
| ------- | ---- | ---- | ----|
| coppa   | int  | no   | Whether or not subject to COPPA rules, `0:no, 1:yes`, if not set, the default value is `1` |
| ext     | RegsExt object |  no  | extended object |

#### RegsExt information

| parameter | type | mandatory | description |
| ------- | ---- | ----| -----|
| gdpr    | int  | no  | Whether it conforms to the GDPR rule, `0: No, 1: Yes`, the default value is `0` |

##### Ad information

| parameter       | type   | mandatory | description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| --------------- | ------ | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type            | int    | yes       | Ad type, 0: banner, 1: interstitial, 2:splash, 3: native, 4:video                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| place_id        | string | yes       | slot id, is generated by YUMI adx, such as "nsgh7kw2" after you registered your slot on [https://www.yumimobi.com](**https**://www.yumimobi.com)                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| floor_price     | float  | no        | Floor price, cent as unit                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| currency        | string | no        | currency, values are "CNY" or "USD", will be mandatory when above `floor_price` has value. Please keep floor_price currency consistent with Company currency, otherwise you won’t be able to get ads.                                                                                                                                                                                                                                                                                                                                                                            |
| w               | int    | yes       | Width of the slot                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| h               | int    | yes       | Height of the slot                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| pos             | int    | no        | Ad position, 0:unknown, 4:head, 5:foot, 6: sidebar, 7:full screen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| inventory_types | array  | no        | types of material. Inventory types are different per different type(ad type). <br>For banner & splash types, the inventory_types should be 1: image, 2: image and text, 4: html5 snippet, 5: text, 7: html5 URL;<br>For interstitial type, the inventory_types should be 1: image, 2: image and text,3: video, 4: html5 snippet, 5: text, 7: html5 URL, 10: playable; <br>For native type, the inventory_types should be 6: native; <br>For video type, the inventory_types should be 3: video, 10: playable; <br>The inventory_types is image by default if this array is null; |
| native          | object | no        | native information                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |

###### Native information

| parameter | type            | mandatory | description                                                                                                      |
| --------- | --------------- | --------- | ---------------------------------------------------------------------------------------------------------------- |
| layout    | int             | yes       | Native types, 1: content wall, 2: app wall, 3:news stream, 4:chat list, 5:scroll ads, 6:content stream, 7:matrix |
| assets    | array of assets | yes       | Native assets, currently there’re five: (title), Icon(img), Large image (img), Description (data), Rating (data) |

**Asset information**

| parameter | type   | mandatory | description                                                         |
| --------- | ------ | --------- | ------------------------------------------------------------------- |
| id        | int    | yes       | element id                                                          |
| required  | int    | no        | Ad element is required or not, 1:required, 0: optional, 0 for fraud |
| title     | object | no        | Title element                                                       |
| img       | object | no        | Image element                                                       |
| data      | object | no        | Other data                                                          |

> an asset only includes an element among of img, title and data.

**Image information**

| parameter | type | mandatory | description                                               |
| --------- | ---- | --------- | --------------------------------------------------------- |
| type      | int  | yes       | Image element type, 1:icon, 2:Logo, 3:picture             |
| w         | int  | no        | Image width, unit: pixel. Value required for native ads.  |
| h         | int  | no        | Image height, unit: pixel. Value required for native ads. |

**Title information**

| parameter | type | mandatory | description     |
| --------- | ---- | --------- | --------------- |
| len       | int  | yes       | length of title |

**Data information**

| parameter | type | mandatory | description                                                                                                                                                                                                                                                                                                                                                                                               |
| --------- | ---- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| type      | int  | yes       | types of data, 1: Sponsor name, should include brand name, 2: description, 3: score, 4: number of likes, 5: number of downloads, 6: price of product, 7: price of sales, always display with price of product together and show user the discount, 8: phone number, 9: address, 10: second description, 11: link that show to user, 12: click-to-action button, 1001: video URL, 1002: number of comments |
| len       | int  | yes       | length of data                                                                                                                                                                                                                                                                                                                                                                                            |

##### Zplay information

| parameter          | type   | mandatory | description                                        |
| ------------------ | ------ | --------- | -------------------------------------------------- |
| app_channel        | string | no        | channel ID                                         |
| uuid               | string | no        | uuid                                               |
| request_id         | string | no        | request_id                                         |
| preload            | int    | no        | whether interstitial ad needs preload, 0:no, 1:yes |
| banner_interval    | int    | no        | interval for Banner ads, unit is second            |
| intersect_interval | int    | no        | interval for interstitial, unit is second          |
| splash_interval    | int    | no        | interval for splash, unit is second                |
| is_close           | int    | no        | whether the ads can be closed, 0: no, 1: yes       |
| ad_loc_id          | string | no        | slot id                                            |
| ios_idfv           | string | no        | iOS idfv                                           |
| open_uuid          | string | no        | open_uuid                                          |

### response

#### Response field

| parameter | type             | mandatory | description                                                       |
| --------- | ---------------- | --------- | ----------------------------------------------------------------- |
| result    | int              | yes       | Return result, 0:success, <0: failure                             |
| msg       | string           | no        | Failure message will be presented if fails, e.g.”internet error”. |
| ad        | object           | no        | No data if it fails or no ads                                     |
| ads       | array of objects | no        | No data if it fails or no ads                                     |
| cur       | string           | no        | currency, values are "CNY" or "USD", default is "CNY"             |

##### Ad information

| parameter          | type     | mandatory | description                                                                                                                                                                                                                                                                              |
| ------------------ | -------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id                 | string   | yes       | ad id                                                                                                                                                                                                                                                                                    |
| place_id           | string   | yes       | slot id, is same with the place_id in request                                                                                                                                                                                                                                            |
| action             | int      | yes       | types of action, 1: open the target_url within WebView in-app, 2: open the target_url within system browser, 3: open map, 4: open dial, 5: play video, 6: download App, 7: arouse App, 8: open application market, make sure to open App Store or Google Play in the app                 |
| html_snippet       | string   | no        | html snippet                                                                                                                                                                                                                                                                             |
| image_url          | string   | no        | image URL                                                                                                                                                                                                                                                                                |
| w                  | int      | yes       | material width                                                                                                                                                                                                                                                                           |
| h                  | int      | yes       | material height                                                                                                                                                                                                                                                                          |
| app_bundle         | string   | no        | App packageName for Android, Bundle identifier for iOS, e.g.: “com.zplay.demo”, app promotion requires                                                                                                                                                                                   |
| store_bundle       | string   | no        | appStorePackageName （Only for Android app）                                                                                                                                                                                                                                             |
| app_ver            | string   | no        | application version                                                                                                                                                                                                                                                                      |
| target_url         | string   | no        | target URL which is the jumping URL when user tap the ads                                                                                                                                                                                                                                |
| click_trackers     | array    | no        | reporting URLs when users click ads                                                                                                                                                                                                                                                      |
| imp_trackers       | array    | no        | reporting URLs when ads are shown                                                                                                                                                                                                                                                        |
| close_trackers     | array    | no        | reporting URLs when users close ads                                                                                                                                                                                                                                                      |
| app_download_trackers | array | no        | track the the URL list when downloading the advertisement APP，should be visited at backstage (only for Android app)|
| app_download_finish_trackers  | array| no | track the the URL list when the advertisement APP download is completed，should be visited at backstage (only for Android app)|
| app_activate_trackers | array | no        | track the the URL list when the advertisement APP is activated，should be visited at backstage (only for Android app)|

| refresh_interval   | int      | yes       | Refresh the ad after the interval, do not refresh if it is 0                                                                                                                                                                                                                             |
| inventory_type     | int      | yes       | types of material, 1: image, 2: image and text, 3: video, 4: html5 snippet, 5: text, 6: native, 7: html5 URL, 10: playable                                                                                                                                                               |
| title              | string   | no        | title of ads of image and text                                                                                                                                                                                                                                                           |
| desc               | string   | no        | description of ads of image and text                                                                                                                                                                                                                                                     |
| ssp_id             | string   | yes       | ssp id, is only used for YUMI internal platform                                                                                                                                                                                                                                          |
| download_file_name | string   | no        | Download file name, required when the action type is download                                                                                                                                                                                                                            |
| file_size          | int      | no        | File size when it is download file                                                                                                                                                                                                                                                       |
| price              | float    | no        | Ad price                                                                                                                                                                                                                                                                                 |
| ex_param           | []string | no        | Expand parameter                                                                                                                                                                                                                                                                         |
| ssp_ad_id          | string   | no        | is only used for YUMI internal platform                                                                                                                                                                                                                                                  |
| video              | object   | no        | video object                                                                                                                                                                                                                                                                             |
| native             | object   | no        | native object                                                                                                                                                                                                                                                                            |
| logo_url           | string   | no        | Buyer’s logo url                                                                                                                                                                                                                                                                         |
| zplay              | object   | no        | is only used for YUMI internal platform                                                                                                                                                                                                                                                  |
| fallback_url       | string   | no        | jumping url that when arousing app failed                                                                                                                                   |
| fallback_action    | int      | no        | action type of fallback_url, 1: open the fallback_url within WebView in-app, 2: open the fallback_url within system browser, 3: open map, 4: open dial, 5: play video, 6: download App, 7: arouse App, 8: open application market, make sure to open App Store or Google Play in the app |

###### Video information

| parameter                  | type   | mandatory | description |
| -------------------------- | ------ | --------- | ----------- |
| url                        | string | yes       | video url |
| play_duration              | int    | no        | Video play duration, unit: second |
| player_start_trackers      | array  | no        | Reporting url while video playing |
| player_end_trackers        | array  | no        | Reporting url while video end playing |
| target_page_show_trackers  | array  | no        | Reporting url while presenting the target page(also can be called landing page), should be visited at backstage |
| target_page_click_trackers | array  | no        | Reporting url while clicking the target page(also can be called landing page), should be visited at backstage. |
| target_page_close_trackers | array  | no        | Reporting url while ads closed ,should be visited at backstage. note: the jumping URL when user taps the click button is ad.target_url, this array is just tracking url when clicking. please don't fill in ad.close_trackers when this array is filled in. |
| player_close_trackers      | array  | no        | Reporting url while video close playing                          |
| player_continue_trackers   | array  | no        | Reporting url while video continue playing                       |
| player_restart_trackers    | array  | no        | Reporting url while video restart playing                        |

##### Zplay information

| parameter     | type   | mandatory | description                  |
| ------------- | ------ | --------- | ---------------------------- |
| app_id        | string | no        | app id for zplay ssp         |
| position_sid  | string | no        | position sid for zplay ssp   |
| app_secret    | string | no        | app secret for zplay ssp     |
| trans_data    | string | no        | transport data for zplay ssp |
| deep_link_url | string | no        | deeplink url                 |

###### Native information

| parameter  | type             | mandatory | description                                                                                                 |
| ---------- | ---------------- | --------- | ----------------------------------------------------------------------------------------------------------- |
| assets     | array of objects | yes       | Native ad list,currently supporting 5, (title), icon (img), picture (img), description (data), score (data) |
| imptracker | array            | no        | Impression tracker address array, a 1-pixel picture needs to be returned from SSP                           |
| link       | object           | no        | Target link, default link object, used when there is no link in Assets                                      |

**Asset information**

| parameter | type   | mandatory | description                                                                  |
| --------- | ------ | --------- | ---------------------------------------------------------------------------- |
| id        | int    | yes       | element ID                                                                   |
| required  | int    | no        | Ad element required to be shown or not, 1: required, 0:optional, 0 for fraud |
| title     | object | no        | title element                                                                |
| img       | object | no        | image element                                                                |
| data      | object | no        | other data                                                                   |
| link      | object | no        | target link                                                                  |

**Image information**

| parameter | type   | mandatory | description               |
| --------- | ------ | --------- | ------------------------- |
| url       | string | yes       | image url                 |
| w         | int    | no        | Image width, unit: pixel  |
| h         | int    | no        | Image height, unit: pixel |

**Title information**

| parameter | type   | mandatory | description |
| --------- | ------ | --------- | ----------- |
| text      | string | yes       | text        |

**Data information**

| parameter | type   | mandatory | description |
| --------- | ------ | --------- | ----------- |
| label     | string | no        | data name   |
| value     | string | yes       | data text   |

**Link information**

| parameter       | type   | mandatory | description                                                                                                                                                                                                                                                                              |
| --------------- | ------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| url             | string | yes       | Target link                                                                                                                                                                                                                                                                              |
| clicktracker    | array  | no        | Click tracker link                                                                                                                                                                                                                                                                       |
| type            | int    | no        | types of action, 1: open the url within WebView in-app, 2: open the url within system browser, 3: open map, 4: open dial, 5: play video, 6: download App, 7: arouse App, 8: open application market, make sure to open App Store or Google Play in the app                               |
| fallback_url    | string | no        | jumping url that when arousing app failed                                                                                                                                   |
| fallback_action | int    | no        | action type of fallback_url, 1: open the fallback_url within WebView in-app, 2: open the fallback_url within system browser, 3: open map, 4: open dial, 5: play video, 6: download App, 7: arouse App, 8: open application market, make sure to open App Store or Google Play in the app |

### Report click-macro information

> When Ad has been Start_play, end_play, show, clicked, Closed, client shall substitute macro variables of click_tracking url, target_url and Video information_url when reporting (if macro variable is existed) in pixels. The variables which need to be substituted are as follows:

| macros                          | type  | description                                                                                                                                                                              |
| ------------------------------- | ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| YUMI_ADSERVICE_CLICK_DOWN_X     | int32 | x-coordinate of finger pressing in the click_tracking url and target_url                                                                                                                 |
| YUMI_ADSERVICE_CLICK_DOWN_Y     | int32 | y-coordinate of finger pressing in the click_tracking url and target_url                                                                                                                 |
| YUMI_ADSERVICE_CLICK_UP_X       | int32 | x-coordinate of finger rising in the click_tracking url and target_url                                                                                                                   |
| YUMI_ADSERVICE_CLICK_UP_Y       | int32 | y-coordinate of finger rising in the click_tracking url and target_url                                                                                                                   |
| YUMI_ADSERVICE_UNIX_ORIGIN_TIME | int32 | Event occurs unix timestamp (ms) in the player_start_trackers url, player_end_trackers url, target_page_show_trackers url ,target_page_click_trackers url and target_page_close_trackers |
| YUMI_ADSERVICE_CUR_TIME         | int32 | The current playback progress (seconds) when the video is Closed                                                                                                                         |
| YUMI_ADSERVICE_START_TIME       | int32 | The progress (seconds) when playback starts again after the video is turned off                                                                                                          |

> When ad display orientation conforms to device screen, the upper left corner of ad unit locates at (0,0), as below. If it is not available, please substitute it to -999.

![click area](/img/click_area.png)
