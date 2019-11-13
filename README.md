# 推啊小程序媒体对接

## 修订记录

|编号|内容|修订时间|影响范围|
|---|---|---|--|---|
|1|测试版|2019-11-13|-|

## 对接流程

1. 合作方媒体在推啊媒体平台 (https://ssp.tuia.cn) 注册账号
2. 创建广告位，在后台获取 appKey、adslotId 等参数

## 小程序跳转

* 推啊小程序的appId 为 
  ```
  2019102868708522
  ```

* 小程序跳转方法

  ```
  my.navigateToMiniProgram({
      appId: '2019102868708522',
      extraData:{
        "appKey": "your appKey",
        "adslotId": "your adslotId"
      },
      success: (res) => {
        console.log(res)
      },
      fail: (res) => {
        console.log(res)
      }
    });
  ```
  具体用法可以参见 [my.navigateToMiniProgram](https://docs.alipay.com/mini/api/yz6gnx)

  ***
  *注意:*
  >  其中, ```extraData```中 ```appKey``` 和 ```adslotId``` 为必传参数.

  >  如果不传或者key传错，会展示测试广告位。

  >  如果value传错，会是空白页面。开发时，请注意测试。