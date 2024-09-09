FROM debian:bullseye

FROM debian:bullseye

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install mariadb-server -y

RUN mkdir -p /var/run/mysqld
RUN chown -R mysql:mysql /var/run/mysqld
RUN chmod 777 /var/run/mysqld

COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/


COPY ./tools/script.sh /
RUN chmod 777 script.sh

EXPOSE 3306

CMD ["/script.sh"]
