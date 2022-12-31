# simple-gorilla_mux.go

「gorilla/mux」に関する学習目的プログラム。  
[gorilla](https://github.com/gorilla/mux)  

## 実行方法

```shell
# デバグ実行
go run main.go

# ビルド
go build -o bin main.go
```

## 実行方法(Docker)

```shell
# Dockerfileのビルドの実行
docker build -t simple-gorilla_mux-go .
docker run -p 80:80 -it --rm --name my-simple-gorilla_mux-go simple-gorilla_mux-go

# 一行で書くなら、、、
docker build -t simple-gorilla_mux-go . && docker run -p 80:80 -it --rm --name my-simple-gorilla_mux-go simple-gorilla_mux-go
```

## 動作確認

以下のパスにアクセスする。  

- /
- /greet
- /customers
- /customers_xml
- /customers_flex
- /methods

customers系には`Accept`ヘッダを`text/xml`と`application/json`に変えてリクエストを送信。  

methodsには複数のHTTPメソッドでリクエストを送信。  

## メモ

プログラムファイルにてあるパッケージをインポートし、「go mod tidy」を実行すると自動でダウンロードしてくれる!!!  

## デプロイ設定(Render.com)

| キー | バリュー |
| ---- | ---- |
| Name | simple-gorilla_mux.go |
| Region | Oregon(US West) |
| Branch | main |
| Root Directory |  |
| Environment | Docker |
| Dockerfile Path | ./Dockerfile |
| Docker Build Context Directory |  |
| Docker Command |  |

## 参考文献

- <https://www.udemy.com/share/103PE43@JyZWqaqer4WCJGGiYgQalepcfxVW38cHTmN7p5IyKIbP0xHR4WVlUMYrBZDi_oGr8g==/>
