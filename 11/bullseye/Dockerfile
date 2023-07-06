FROM postgres:11-bullseye

RUN apt-get update && apt-get install -y --no-install-recommends \
    postgresql-11-cron

CMD ["-c", "shared_preload_libraries=pg_cron", "-c", "cron.database_name=postgres"]