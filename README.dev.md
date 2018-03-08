# Setup for Developers

## Basics

This Application is build using the [Play framework](https://playframework.com/).
The Language used for the Backend ist [Scala](https://www.scala-lang.org/).
The Frontend is implemented using the [Angular](https://angular.io/) with [TypeScript](https://www.typescriptlang.org/).

If you want to start developing for this application you should become acquainted with Play, Scala, Angular and TypeScript. 

### Docker

The development and deployment will relay strongly on [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/).
It is necessary for docker and docker-compose to be installed and running.

### sbt

during the development you might need to use the scala build tool ([sbt](https://www.scala-sbt.org/)).
Using the docker container Sbt can run without being installed on your machine as described here:

```bash
docker run --rm -it -v $PWD:/sbt -v $HOME:/cache -u $(id -u):$(id -g) dstulle/sbt
```

The first execution might take a bit longer because sbt does some downloads but they will be cached during the following runs.

Alternatively you can install and run sbt on your local machine.

### npm

TODO

## Starting the development server

To start the Development Server just run the development docker-compose-file:

```bash
docker-compose -f docker-compose.dev.yml up --build
```

After this you should be able to navigate your favorite browser to [http://localhost:9000/](http://localhost:9000/) and se the application.
