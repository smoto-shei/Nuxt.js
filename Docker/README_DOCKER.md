# Vue 側

0. frontend に移動
1. イメージ作成

- docker build -t just_img:0620 .

2. コンテナ作成(pwd はマウントさせる場所。clone して、frontend に移動して実行する。)

- docker run -v `pwd`:/app -p 3000:3000 --name jest_ctn -it -d  jest_img:0620

※ コンテナ作成済みの場合 → コンテナ開始

- docker start v_mojiokoshi

3. コンテナの起動確認

- docker ps

4. コンテナに入る

- docker exec -it v_mojiokoshi sh

5. イニシャライズ(初回のみ)

- npm install

6. 開発環境の起動

- npm run serve

7. コンテナ停止 npm

- docker stop v_mojiokoshi

# Flask 側

0. backend に移動
1. イメージ作成

- docker build -t flask_env .

2. コンテナ作成

- docker run -v `pwd`:/mojiokoshi -p 5000:5000 --name f_mojiokoshi -it -d flask_env

※ コンテナ作成済みの場合 → 開始

- docker start f_mojiokoshi

3. コンテナの起動確認

- docker ps

4. コンテナに入る

- docker exec -it f_mojiokoshi sh

5. 環境変数を通す(GCP のキーがある json ファイル名に変更)

- export GOOGLE_APPLICATION_CREDENTIALS="/mojiokoshi/npl-mojiokoshi.json"

※ LB のバケットのアクセスキー

- export GOOGLE_APPLICATION_CREDENTIALS="/mojiokoshi/nlp-mojiokoshi-86e392a2171a.json"

※ 今成のローカルなら

- export GOOGLE_APPLICATION_CREDENTIALS="/Users/yuya/Downloads/MyFirstProject.json"

6. flask 起動

- python run.py

7. コンテナ停止

- docker stop f_mojiokoshi

## 補足

コンテナ一覧

- docker ps -a

コンテナ削除

- docker rm コンテナ名 or ID

イメージ一覧

- docker images

イメージ削除(イメージをもとに作成されたコンテナがある場合、まずコンテナを削除する必要がある)

- docker rmi images 名 or ID

停止

- docker stop mojiokoshi

開始

- docker start mojiokoshi

※ 今成用メモ

- export GOOGLE_APPLICATION_CREDENTIALS="/Users/yuya/Mac/Web/mojiokoshi/backend/nlp-mojiokoshi-86e392a2171a.json"
