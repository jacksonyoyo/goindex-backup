![GoIndex](https://raw.githubusercontent.com/jacksonyoyo/goindex-backup/master/themes/logo.png)  

GoIndex

基于 [Cloudflare Workers](https://workers.cloudflare.com/) 和 [Google Drive](https://www.google.com/drive/) 的功能，你可以部署你的代碼在 Cloudflare Workers ，實現以目錄形式展示 Google Drive 中的文件。

`index.js` 包含 Workers 所需的代碼.  

## Demo


## 安裝部署方案1
1、在本地安裝 rclone

2、按照 https://rclone.org/drive/ 流程進行授權。

3、執行 rclone config file 查看 rclone.conf 路徑。找到root_folder_id和refresh_token記錄下來。

4、下載 https://github.com/donwa/goindex 中的 index.js  并填入 root 和 refresh_token

5、復制代碼 到 CloudFlare 部署。


## 安裝部署方案2 (快速自動)

作者不會記錄refresh_token，但為避免糾紛，建議有條件的使用方案1進行部署
1、訪問[goindex-install.yoyosky.workers.dev](https://goindex-install.yoyosky.workers.dev/) 
2、授權認證后，生成部署代碼。
3、復制代碼 到 CloudFlare 部署。  
## 文件夾密碼：
在google drive 文件中放置 `.password` 文件來設置密碼。  

密碼文件只能保護該文件不被列舉，不能保護該文件夾的子文件夾不被列舉。

也不保護文件夾下文件不被下載。

程序文件中 `root_pass` 只為根目錄密碼，優先于 `.password` 文件

## 更新日志

1.0.6
添加 classic 模板

1.0.5
添加文件展示頁

1.0.4
修復 注入問題。

1.0.3
修復 `.password` 繞過下載問題。

1.0.2 
優化前端邏輯  
添加文件預覽功能(臨時) 
添加前端文件緩存功能 

1.0.1
添加 README.md 、 HEAD.md 支持

1.0.0
前后端分離，確定基本架構 
添加.password 支持 

*********************************************************************************

前几天我突然发现自己的 goindex 网页打开是一片空白，然后才知道 donwa 大佬删库了，于是我找了其他的仓库部署了一下网页，今天偶然发现网页打不开是有解决办法的，看到了一篇博文，所以就赶快修改了自己的代码，非常感谢，下面是解决方法，另外博文参考自：
- 解决goindex作者删库，导致goindex打不开的问题 - 天下无鱼  https://shikey.com/2020/04/27/goindex-index-js-repack.html
## 解决方法：
- 【可选】首先到 GitHub Fork一份 Goindex 的代码。
- 登录CF，打开workers，选中项目修改原代码部分的一行即可。具体操作如下 —— 找到以下代码，一般是在 21行/23行 。

![cf代码修改细节](https://ae01.alicdn.com/kf/U324911b4bfea4f5bbd01d83026575b51d.png)
！图片加载不出来可直接访问：http://dwz.date/awtQ

### 另外我发现 goindex 现在的版本可以看 GD 快捷方式的文件了，这样就可以把别人共享的文件直接创建快捷方式，在自己的网页看，非常 nice 。


PS：以下内容为原始内容。
![GoIndex](https://raw.githubusercontent.com/donwa/goindex/master/themes/logo.png)  
  
GoIndex
Google Drive Directory Index  
Combining the power of [Cloudflare Workers](https://workers.cloudflare.com/) and [Google Drive](https://www.google.com/drive/) will allow you to index you files on the browser on Cloudflare Workers.    

`index.js` is the content of the Workers script.  

## Demo  
material: [https://index.gd.workers.dev/](https://index.gd.workers.dev/)  
classic: [https://indexc.gd.workers.dev/](https://indexc.gd.workers.dev/)  

## Deployment  
1.Install `rclone` software locally  
2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  
3.Execute the command`rclone config file` to find the file `rclone.conf` path  
4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  
5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  
6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## Quick Deployment  
1.Open https://installen.gd.workers.dev/  
2.Auth and get the code  
3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  

## About  
Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  
