FROM postgres:15-bookworm

RUN apt-get update && apt-get install -y --no-install-recommends \
    postgresql-15-cron

CMD ["-c", "shared_preload_libraries=pg_cron", "-c", "cron.database_name=postgres"]