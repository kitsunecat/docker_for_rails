# docker_for_railsの使い方
## git cloneせにゃ
`git clone git@github.com:kitsunecat/docker_for_rails.git`

## ディレクトリ移動
`cd docker_for_rails`

## とりあえずdockerビルド
`docker-compose build`

## docker起動
`docker-compose up`
- オプション`-d`をつけたらバックグラウンド起動
- `docker-compose down`でdocker停止

## アクセスして確認
http://0.0.0.0:3000 にアクセスしてYay!の画面が出てくるはず

## こんなときはもう一度dockerビルド
- gemの追加（Gemfileの変更）
- ミドルウェア等の追加(apt-getで追加するなど)

### ミドルウェアの追加について
Dockerfileの7行目あたりから
`RUN apt-get -y install <追加するアプリ名>`みたいな感じで追加してからビルドしなおしてください
