FROM mysql:8.0
RUN adduser -r expense
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_USER=expense \
    MYSQL_DATABASE=transactions
# COPY scripts/*.sql /docker-entrypoint-initdb.d/
RUN chown -R expense:expense /var/lib/mysql /var/run/mysqld
COPY scripts/*.sql /docker-entrypoint-initdb.d/
USER expense