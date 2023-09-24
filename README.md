# ECS-NGINX

## M#MO

```js
// コマンドからリポジトリを作成する場合（ｋブラウザｋ良い）
$ aws ecr create-repository --repository-name [作成するリポジトリ名] --profile [profile指定があれば]
// ECSのdockerにｓログインするコマンド
$ aws ecr get-login-password --region ap-northeast-1 --profile [profile指定があれば] | docker login --username AWS --password-stdin [リポジトリのURL] 

// イメージの作成
docker build -t [コンテナ名] .

// イメージにタグを付ける
docker tag [コンテナ名]:latest [リポジトリのURL]:latest

// PUSHする
docker push [リポジトリのURL]latest
```
