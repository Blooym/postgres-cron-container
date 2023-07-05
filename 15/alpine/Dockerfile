FROM postgres:15-alpine

RUN apk add --no-cache postgresql-pg_cron sudo \
    && cp /usr/lib/postgresql15/pg_cron.so /usr/local/lib/postgresql/ \
    && cp /usr/share/postgresql/extension/* /usr/local/share/postgresql/extension

CMD ["-c", "shared_preload_libraries=pg_cron", "-c", "cron.database_name=postgres"]