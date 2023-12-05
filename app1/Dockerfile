FROM nginx
RUN  apt update && \
apt install php-fpm -y && \
apt install php-mysql -y

COPY ./default.conf /etc/nginx/conf.d/default.conf
COPY ./www.conf /etc/php/8.2/fpm/pool.d/www.conf
COPY ./php.ini /etc/php/8.2/cli/php.ini
COPY ./html/ /usr/share/nginx/html/
EXPOSE 80
ADD run.sh /
RUN chmod +x /run.sh
CMD bash /run.sh
