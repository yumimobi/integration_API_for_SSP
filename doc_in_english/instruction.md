# STEPS OF INTEGRATION

1. introduce your application information

    include but not limit app name, app bundle ID or package name, download URL, snapshot of ad_slot, types of material(jpg, jpeg, png, gif, html and so on）, whether multi-URLS can be reported, whether caching can be allowed, whether deeplink is supported and so on, YUMI Adx evaluates the integration's priority and importance through these information.

2. get your account

    - first of all, contact YUMI account manager and confirm the cooperation.
    - second, click `publishers` button on [https://www.yumimobi.com/en/index.html](https://www.yumimobi.com/en/index.html) and register your account. after registered, please offer your mail that you registered to YUMI account manager.
    - the last, YUMI account manager will give you SSP Token after your account have been approved.

3. understand integration documentation

    view [request and response](request_and_response.md) to understand YUMI documentation, for reference, please view [sample of request and response](sample_of_request_and_response.md)

4. develop and test

    develop according above documentation and test using testing token and app ID. if the ad shows normally, the integration would be successful.

 

  > testing token is ``EXVTAW2VYMKUY30TBGLUZ3XPC3H2YW6NQHPWBGF6LMNVBTA6LK9YNS6PMJAUNZG=`` 

> testing APP ID：

OS | APP ID |Slot Format| Slot ID 
- | :-: | :-: | :-: | :-: |
 Android| bg76gil7 | banner | an6o1ngv 
 Android| bg76gil7 | Interstitial| 13ohe4ze 
 Android| bg76gil7 | Reawrd Video| dsdibu5j 
 Android| bg76gil7 | Native|13ur17b0
 Android| bg76gil7 | Splash| 50otuc9h
iOS| yywtptfq | banner | 5jr45zcy 
 iOS| yywtptfq | Interstitial| n0w2zkex 
 iOS| yywtptfq | Reawrd Video| hmtdjpt4 
 iOS| yywtptfq | Native|gk8cmfh8
iOS| yywtptfq| Splash|ss03ye17

5. Test with a little online inventory and confirm the statistics data

6. deploy the integration
