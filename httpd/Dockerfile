FROM alpine:latest
MAINTAINER SaltyDev42

USER root
RUN apk add apache2
RUN sed -i.bak 's/Listen 80/Listen 8080/g' /etc/apache2/httpd.conf
RUN chown apache:apache /var/log/apache2 /usr/lib/apache2 /run/apache2 && \
    chmod 700 /var/log/apache2 /usr/lib/apache2 /run/apache2

USER apache
EXPOSE 8080
CMD ["httpd", "-DFOREGROUND"]
