##　環境構築
1. docker-compose.yml、app/Dockerfile、app/Gemfileを用意する
1. docker-compose upでコンテナをビルド、立ち上げ
1. docker container exec -it railstutorial_web_1 bashでコンテナに入る
1. コンテナ内でrails new ./をしてrailsの環境を作る
1. web/config/database.ymlのhostをdbに変更する
1. コンテナ内でrails db:create

