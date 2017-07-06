# docker-travis-cli

Simple image for running the Travis-CI cli through Docker.

## Retrieving the image

Retrieving the Docker image is simple:

    docker pull garbetjie/travis:latest

## Using the image

Making use of the image is best done using a shell alias. For example, zsh and bash users can use the following alias to alias `travis` to the docker image:

    alias travis="docker run --rm -ti -v \$PWD:/project -v ~/.travis:/travis garbetjie/travis:latest"

This will ensure that every time you run the `travis` command, it will transparently run it as this Docker image.

## Different versions

You can replace the `:latest` in the alias above for a specific version of the Travis-CI cli, if required.
For example, this is how an alias for version 1.8.8 would look:

    alias travis="docker run --rm -ti -v \$PWD:/project -v ~/.travis:/travis garbetjie/travis:1.8.8"
