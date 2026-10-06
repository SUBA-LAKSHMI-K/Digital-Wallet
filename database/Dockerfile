FROM mysql:8.0

ENV MYSQL_ROOT_PASSWORD=Root@12345
ENV MYSQL_DATABASE=digital_wallet

COPY schema.sql /docker-entrypoint-initdb.d/01_schema.sql
COPY functions.sql /docker-entrypoint-initdb.d/02_functions.sql
COPY procedures.sql /docker-entrypoint-initdb.d/03_procedures.sql
COPY triggers.sql /docker-entrypoint-initdb.d/04_triggers.sql
COPY data.sql /docker-entrypoint-initdb.d/05_data.sql

EXPOSE 3306