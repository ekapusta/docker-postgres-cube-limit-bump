# Latest official Postgres with Cube limit bumped

By default CUBE allows no more, than 100 dimensions.

This image allows you to bump it to 128 by changing `CUBE_MAX_DIM` and recompiling `cube.so`.

## Build

    docker build --tag=ekapusta/postgres-cube-limit-bump .

## Debug

    docker run --rm --interactive --tty ekapusta/postgres-cube-limit-bump bash
    docker run --rm -p 5432:5432 --name postgres -e POSTGRES_PASSWORD=mysecretpassword ekapusta/postgres-cube-limit-bump
