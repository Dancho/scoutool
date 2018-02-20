FROM java:9-jre

MAINTAINER Daniel Sturm <mail@danielsturm.de>

COPY build.properties /project/

RUN set -x \
 && apt-get update \
 && apt-get install -y \
    gnupg \
    apt-transport-https \
 && echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list \
 && apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823 \
 && apt-get update \
 && apt-get install -y \
    sbt \
 && ln -s /usr/lib/jvm/java-9-openjdk-amd64/lib /usr/lib/jvm/java-9-openjdk-amd64/conf \
 && sbt sbtVersion

VOLUME ["/app"]
WORKDIR /app

ENTRYPOINT ["sbt"]