# logrotate-sidecar

容器化後，如果在部分場景下需要 roate 容器內的 Log檔，可以使用本範例來去進行修改調整，logrotate 核心功能為原作者所有

## 使用方式

部署 YAML 檔案
```
kubectl apply -f .
```

開啟瀏覽器，並且將首頁的「Auto Refresh」打勾，讓服務持續產生 Access Log
```
http://127.0.0.1:9453
```

此時可以進入 Nginx 容器內 `/var/log/nginx/` 確認是否有 log 產生，並且也進入 logrotate 容器內 `/var/log/custom` 是否有相同的檔案

## 其他說明

logrotate 核心功能變數調整，可以參考原作者的說明

https://hub.docker.com/r/blacklabelops/logrotate
