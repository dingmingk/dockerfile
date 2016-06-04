FROM java:openjdk-8-jdk
MAINTAINER dingmingk <dingmingk@gmail.com>

ENV ANT_VERSION 1.9.7
ENV ANT_HOME /opt/ant

RUN mkdir -p $ANT_HOME \
  && curl -fsSL https://github.com/apache/ant/archive/rel/${ANT_VERSION}.tar.gz \
    | tar -xzC $ANT_HOME --strip-components=1

ENV PATH $PATH:$ANT_HOME/bin
WORKDIR /project

ENTRYPOINT ["ant"]
CMD ["-h"]
