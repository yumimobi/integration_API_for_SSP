# CHECK LIST AFTER INTEGRATION

## 1. sending the UA and IP address of client

please confirm you send the `UA` and `IP address` of client to YUMI Adx through `http header` when you send a request to YUMI Adx.

## 2. about tracking URL reporting

- all of tracking URLs must be reported through client side, not allowed through server side.
- please confirm all URLs that `imp_trackers` and `click_trackers` includes can be reported.

> your revenue will be affected if there are tracking URL didn't report successfully.
