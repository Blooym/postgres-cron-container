# postgres-extended

A repackaged PostgresSQL container image with additioanl extensions bundled inside and set up for use.

## Extensions
- [pg_cron](https://github.com/citusdata/pg_cron) - A cron-like scheduler for PostgresSQL, installed from a package repository or built from source depending on package availability.

## Updates

All images are updated automatically every day and are kept as close to the [base Postgres image](https://hub.docker.com/_/postgres) as possible. Images may not be 1:1 compatiable with the base image and are maintained on a best-effort basis.

## Usage

Check out the package page [here](https://github.com/Blooym/postgres-extended/pkgs/container/postgres-extended) for all available tags. The tags are named in the format of `postgres-extended:<postgres-version>-<distro>`.
