# ベースイメージを指定
FROM ruby:3.1.2

# 必要なパッケージをインストール
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

# 作業ディレクトリを設定
WORKDIR /myapp

# GemfileとGemfile.lockをコピー
COPY ./hello_world_app/Gemfile ./hello_world_app/Gemfile.lock ./

# Bundlerをインストールして依存関係を解決
RUN gem install bundler && bundle install

# アプリケーションの全ファイルをコピー
COPY . .

# サーバーを起動
CMD ["rails", "server", "-b", "0.0.0.0"]
