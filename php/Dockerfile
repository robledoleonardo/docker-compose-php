FROM php:7.0-fpm-jessie
# Install modules
RUN apt-get update && apt-get install -y \
	libfreetype6-dev \
	libjpeg62-turbo-dev \
	libmcrypt-dev  \
	libpng-dev \
	libicu-dev \
	mysql-client \
	&& docker-php-ext-install pdo_mysql \
	&& docker-php-ext-install iconv \
	&& docker-php-ext-configure mcrypt \
	&& docker-php-ext-install mcrypt \
	&& docker-php-ext-install intl \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install gd \
	&& docker-php-ext-install opcache \
	&& docker-php-ext-install mbstring 
CMD ["php-fpm"]