# github-star-trend

基于Github API实现的一个Chrome插件，在访问github项目的时候，会自动注入一个Star Trend按钮，点击可以查看该项目自创建以来star增长的一个趋势图。

## 预览

![preview](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/github-star-trend/demo.gif)

## 使用

1. 下载项目zip并解压为文件夹`github-star-trend`。

2. 打开Chrome浏览器，地址栏中输入[chrome://extensions/](chrome://extensions/)，选择`加载已解压的扩展程序`，并选择该文件夹目录即可。

![guide](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/github-star-trend/guide.jpg)

## 注意

由于插件是基于Github API中[Starring](https://docs.github.com/zh/rest/activity/starring)实现的，且Github对同一IP的调用频次有[限制](https://docs.github.com/zh/rest/using-the-rest-api/rate-limits-for-the-rest-api)(1小时60次)。所以在使用次数过多时，有如下的提示，此时你可以在登录GitHub后访问[https://github.com/settings/tokens](https://github.com/settings/tokens)申请一个[Access Token](https://github.com/settings/personal-access-tokens)来突破该限制(1小时5000次)，申请时的`Expiration`也就是到期时间改成`Not expiration`。另外，在浏览器F12找到Application即可看到，`Access Token`会被保存在Local Storage中键为`STAR_TREND_ACCESS_TOKEN`的值的地方。需要修改可在此更改，如果没有该键值对则说明你还未超过以上1小时60次限制。

![warn](https://cdn.jsdelivr.net/gh/rawchen/JsDelivr/static/github-star-trend/warn.png)

## License

[MIT协议](./LICENSE)