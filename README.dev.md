# Setup for Developers

This Application is build using the ([play framework](https://playframework.com/)).

To develop you might need to install the scala build tool ([sbt](https://www.scala-sbt.org/)). sbt can be install directly to your machine or be used within a docker container

## sbt container

to run `sbt` on any machine without installing it just run it with docker

2. Running the container:
```
    docker run --rm -it -v $PWD:/sbt -v $HOME:/cache -u $(id -u):$(id -g) dstulle/sbt
```

The first execution might take a bit longer because sbt does some downloads but they will be cached during the following runs.
