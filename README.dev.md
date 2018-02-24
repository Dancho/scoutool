# Setup for Developers

## Basics

This Application is build using the ([play framework](https://playframework.com/)).

To develop you might need to install the scala build tool ([sbt](https://www.scala-sbt.org/)).
Sbt can also be used within a docker container as described here:

```bash
docker run --rm -it -v $PWD:/sbt -v $HOME:/cache -u $(id -u):$(id -g) dstulle/sbt
```

The first execution might take a bit longer because sbt does some downloads but they will be cached during the following runs.

## Starting the development server

To start the Development Server there are two ways.

If sbt is installed on your machine just type:

```bash
sbt run
```

Or if docker is installed just type:

```bash
docker-compose -f docker-compose.dev.yml up --build
```

After this you should be able to navigate your favorite browser to [http://localhost:9000/](http://localhost:9000/) and se the application.
