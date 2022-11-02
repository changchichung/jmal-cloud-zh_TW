```
### clone jma-cloud-view 原始程式
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
