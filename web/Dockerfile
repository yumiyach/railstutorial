FROM arm64v8/ruby:3.2.2 
#↑arm64v8がすげー大事

#debian系のためapt-getを使用してnode.jsとyarnをインストール
RUN apt-get update -qq
RUN curl -fsSL https://deb.nodesource.com/setup_lts.x | bash - \
&& apt-get install -y nodejs default-mysql-client libpq-dev build-essential
RUN npm install --global yarn

#docker内の作業ディレクトリを作成＆設定
WORKDIR /web

#Gemfile,Gemfile.lockをローカルからCOPY
COPY Gemfile /web/

#コンテナ内にコピーしたGemfileを用いてbundel install
RUN bundle install

#railsを起動する
CMD ["rm", "/web/tmp/pids/server.pid"]
CMD ["rails", "server", "-b", "0.0.0.0"]