# Setup for Developers

This Application is build using the ([play framework](https://playframework.com/)).

To develop you might need to install the scala build tool ([sbt](https://www.scala-sbt.org/)). sbt can be install directly to your machine or be used within a docker container

## sbt container

to run `sbt` on any machine without installing it just build a docker container and run it with docker

1. Building the Container:
```
    docker build -t sbt -f dockerfiles/sbt/Dockerfile dockerfiles/sbt/
```
2. Running the container:
```
    docker run --rm -it -v $PWD:/app -v $PWD/sbt-cache:/root sbt
```

The Container has do be build only once or if the [Dockerfile](dockerfiles/sbt/Dockerfile) has changed.
If the container was build it can be executed at will. The first execution might take a bit longer because sbt does some downloads but they will be cached during the following runs.
