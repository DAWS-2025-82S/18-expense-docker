FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
COPY scripts/*.sql /docker-entrypoint-initdb.d

# docker build -t mysql:1.0.0 .
# docker run -d --name mysql mysql:1.0.0

# docker exec -it mysql bash
# mysql -u root -pExpenseApp@1
# show databases;
# use transactions;
# show tables;

# ifconfig
# docker inspect mysql  # to get container IP