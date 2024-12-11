FROM postgres:14-alpine

ENV PG_CRON_VERSION "1.6.4"

# Build dependencies
RUN apk add --no-cache --virtual .build-deps \ 
    build-base \ 
    clang19 \
    llvm15 \
    tar

# Grab tarball from repository
RUN wget -O /pg_cron.tgz https://github.com/citusdata/pg_cron/archive/v$PG_CRON_VERSION.tar.gz \
    && tar xvzf /pg_cron.tgz

# Build & install
RUN cd pg_cron-$PG_CRON_VERSION \
    && sed -i.bak -e 's/-Werror//g' Makefile \ 
    && sed -i.bak -e 's/-Wno-implicit-fallthrough//g' Makefile \
    && make && make install

# Cleanup
RUN rm -rf pg_cron.tgz && rm -rf pg_cron-* \
    && apk del .build-deps

CMD ["-c", "shared_preload_libraries=pg_cron", "-c", "cron.database_name=postgres"]