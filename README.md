# docker_for_railsの使い方

## とりあえずdockerビルド
`docker-compose build`

## プロジェクト作成
`dcrun web rails new . ＜プロジェクト名＞ --skip-gemfile`
- 途中ででてくる確認は全部`y`ですすめる

## docker起動
`docker-compose up`
- オプション`-d`をつけたらバックグラウンド起動
- `docker-compose down`でdocker停止

## アクセスして確認
http://0.0.0.0:3000 にアクセスしてYay!の画面が出てくるはず
