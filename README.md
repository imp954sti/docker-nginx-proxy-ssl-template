## 概要
[nginx-proxy](https://github.com/jwilder/nginx-proxy)
[docker-letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion)
を使ってSSL対応のマルチドメイン環境を作るためのテンプレートです

## 使い方
app1/docker-compose.ymlの編集
```
VIRTUAL_HOST: <ドメイン>
LETSENCRYPT_HOST: <ドメイン>
LETSENCRYPT_EMAIL: <メールアドレス>
```

## 起動
```
cd nginx-proxy
docker-compose up -d

cd ../app1
docker-compose up -d
```

## サービスを追加する
サービスを増やすときはappフォルダをコピーして
docker-compose.ymlを編集して```docker-compose up -d```する
