# goindex-installer
[GoIndex](https://github.com/donwa/goindex) 之代碼生成器

donwa 的 [GoIndex 代碼生成器](https://install.gd.workers.dev/) 開源版本 !!!

[代碼生成器](https://goindex-install.yoyosky.workers.dev/) goindex-install.yoyosky.workers.dev <<< 開源版本修改成品

## 注意
這里使用的還是[Rclone](https://github.com/rclone/rclone)程序提供的OAuth 2.0客戶端ID和秘鑰，如果你比較介意，可以到[Google API Console](https://console.developers.google.com)申請自己的ID和秘鑰并替換使用

## Demo
[goindex-install.yoyosky.workers.dev/](https://goindex-install.yoyosky.workers.dev/)

## 部署
到[Cloudflare Workers](https://dash.cloudflare.com)創建一個新的Worker，復制[main.js](main.js)中的內容保存并部署即可

## 欲修改自用方式
1.
main.js 中 尋取
const jsURL = 'https://raw.githubusercontent.com/xxxxxx/xxxxxxx/master/index.js'; << 為自身 GoIndex index.js 連結

2.
自身 GoIndex index.js 下
<script src="//cdn.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx,gh/此處/themes/${authConfig.theme}/app.js 為本身所有 GoIndex 帳ID/goindex名

