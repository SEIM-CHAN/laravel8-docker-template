#イメージのベースを指定
FROM php:7.4-fpm

#composerのインストール
COPY --from=composer:1.10 /usr/bin/composer /usr/bin/composer

#パッケージ管理ツールapt-getの更新と必要パッケージのインストール
RUN apt-get update \
&& apt-get install -y \
git \
zip \
unzip \
&& docker-php-ext-install pdo_mysql bcmath

WORKDIR /var/www/html

#コンテナ内に入った時のディレクトリを指定
WORKDIR /var/www/html

#php.iniの記述
COPY ./php.ini /usr/local/etc/php

#node
RUN curl -SL https://deb.nodesource.com/setup_15.x | bash
RUN apt-get install -y nodejs