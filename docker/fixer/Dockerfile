FROM php:8.0-fpm
ADD ./docker/fixer/php-cs-fixer-v2.phar /usr/local/bin/php-cs-fixer
RUN ["chmod", "+x", "/usr/local/bin/php-cs-fixer"]
VOLUME ["/var/www/matomo"]
WORKDIR /var/www/matomo
ENTRYPOINT ["php-cs-fixer"]
CMD ["--version"]
