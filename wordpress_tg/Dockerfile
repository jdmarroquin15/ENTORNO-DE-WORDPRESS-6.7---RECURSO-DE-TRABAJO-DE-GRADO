FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y \
    apache2 \
    php \
    php-mysql \
    php-curl \
    php-gd \
    php-mbstring \
    php-xml \
    php-zip \
    wget \
    unzip \
    curl \
    vim \
    && rm -rf /var/lib/apt/lists/*

RUN rm -f /var/www/html/index.html

RUN wget https://wordpress.org/wordpress-6.7.tar.gz -O /tmp/wordpress.tar.gz \
    && tar -xzf /tmp/wordpress.tar.gz -C /tmp \
    && cp -R /tmp/wordpress/* /var/www/html/ \
    && chown -R www-data:www-data /var/www/html \
    && rm -rf /tmp/wordpress /tmp/wordpress.tar.gz

RUN a2enmod rewrite

RUN sed -i 's/AllowOverride None/AllowOverride All/g' /etc/apache2/apache2.conf

EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]

