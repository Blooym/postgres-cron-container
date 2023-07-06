# postgres-cron-container

A repackaged PostgresSQL docker image with pg_cron bundled inside and automatically setup to run.

## Updates

All images are updated automatically every day and are kept as close to the [base Postgres image](https://hub.docker.com/_/postgres) as possible. Images may not be 1:1 compatiable with the base image and are maintained on a best-effort basis.

`pg_cron` will either be installed from a package repository or built from the [source repository](https://github.com/citusdata/pg_cron) (using a pinned version number) depending on package availability, as such there may be times where different images within the same version of postgres may have different versions of `pg_cron` installed.

## Usage

Check out the package page [here](https://github.com/Blooym/postgres-cron-container/pkgs/container/postgres-cron-container) for all available tags. The tags are named in the format of `postgres-cron-container:<postgres-version>-<distro>`.
