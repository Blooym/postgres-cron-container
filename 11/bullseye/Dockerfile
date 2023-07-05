FROM postgres:11-bullseye

RUN apt-get update && apt-get install -y --no-install-recommends \
    postgresql-15-cron \
    && rm -rf /var/lib/apt/lists/*

CMD ["-c", "shared_preload_libraries=pg_cron", "-c", "cron.database_name=postgres"]