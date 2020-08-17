FROM alpine:latest
MAINTAINER SaltyDev42

USER root
RUN apk add apache2
RUN sed -i.bak 's/Listen 80/Listen 8080/g' /etc/apache2/httpd.conf

USER 1000
EXPOSE 8080
ENTRYPOINT ["httpd"]
CMD ["-DFOREGROUND"]