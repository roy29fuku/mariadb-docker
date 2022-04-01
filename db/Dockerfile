FROM mariadb:10.3

RUN apt update \
    && apt install --no-install-recommends -y tzdata \
    && apt clean

COPY ./conf.d /etc/mysql/conf.d
COPY ./initdb.d /docker-entrypoint-initdb.d

RUN chown -R mysql:mysql /docker-entrypoint-initdb.d

RUN touch /var/log/mysql/mysqld.log
