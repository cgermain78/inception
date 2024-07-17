FROM debian:bullseye

RUN apt update -y
RUN apt upgrade -y
RUN apt-get install mariadb-server -y

COPY conf/50-server.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf

COPY ./conf/mariadb_launch.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/mariadb_launch.sh

ENTRYPOINT ["/usr/local/bin/mariadb_launch.sh"]
