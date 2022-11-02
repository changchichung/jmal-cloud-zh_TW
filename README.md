https://github.com/jamebal/jmal-cloud-view

### jmal-cloud https://github.com/jamebal/jmal-cloud-view

實在是個很不錯用的網盤程式，只是目前(2022/11/01) 作者表示尚不支援多國語系，偏偏看到簡體字又很頭痛
所以就透過 opencc 把 裡面的 js 做了一次簡體轉繁體
但是也只有這樣處理而已，並沒有去做不同用語的轉換 (比如說「视频」-- 「影片」)

因為原本的架構不支援多國語系，所以沒辦法用PR 送回給原作者
所以新建立了這個 repo

用法很簡單，只要先依照 https://github.com/jamebal/jmal-cloud-view 的說明
```````
```
###clone jma-cloud-view 原始程式
git clone --depth=1 https://github.com/jamebal/jmal-cloud-server.git
cd jmal-cloud-server
./jc.sh install
```
然後 clone 這個 repo
再把js 目錄複製到上面clone 下來的jmal-cloud-server 目錄內的 docker/www/dist/static/
覆蓋掉原本的 js 檔案就可以，當然，建議先備份原本的 js
延續上面的指令

```
mv docker/www/dist/static/{js,js.cn}
git clone https://github.com/changchichung/jmal-cloud-zh_TW
cp -R jmal-cloud-zh_TW/js docker/www/dist/static/
```

接著 ```docker-compose down && docker-compose up -d ```重啟 docker 就可以了

