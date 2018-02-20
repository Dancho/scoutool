# scoutool

## Ideas

* Architecture based on [Domain Driven Design](https://en.wikipedia.org/wiki/Domain-driven_design)
* Used Framework will be [Play](https://www.playframework.com/)
* Continuous Integration with [Cloudogu](https://cloudogu.com/)
* git Branching model based on [GitFlow](https://datasift.github.io/gitflow/IntroducingGitFlow.html)

## Setup

to run `sbt` on any machine without installing it just build a docker container and run it with docker

    docker build -t sbt -f dockerfiles/sbt/Dockerfile dockerfiles/sbt/
    docker run --rm -it -v $PWD:/app sbt

