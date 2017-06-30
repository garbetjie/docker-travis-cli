# docker-travis-cli

Simple Docker image for running the `travis-ci` CLI without having to install Ruby.

## Retrieving the image

Retrieving the Docker image is simple:

    docker pull garbetjie/travis:latest

## Using the image

Making use of the image is best done using a shell alias. For example, zsh and bash users can use the following alias to alias `travis` to the docker image:

    alias travis="docker run --rm -ti -v $PWD:/project -v ~/.travis:/travis garbetjie/travis:latest"

This will ensure that every time you run the `travis` command, it will transparently run it as this Docker image.
