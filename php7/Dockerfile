FROM php:7.4.2-fpm
RUN apt-get update \
  && docker-php-ext-install pdo_mysql mysqli \
  # 手動安裝依賴
  && apt-get install -y libmemcached-dev zlib1g-dev \
  # 安裝需要的擴充套件
  && pecl install memcached-3.1.5 \
  # 啟用擴充套件
  && docker-php-ext-enable memcached
WORKDIR /var/www/html
EXPOSE 9000
