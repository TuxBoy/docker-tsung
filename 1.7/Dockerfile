FROM erlang:18

MAINTAINER Andrea Usuelli <andreausu@gmail.com>

RUN apt-get update && \
    apt-get install -y python perl libtemplate-perl gnuplot && \
    curl http://tsung.erlang-projects.org/dist/tsung-1.7.0.tar.gz --output /tmp/tsung-1.7.0.tar.gz \
    && cd /tmp/ \
    && tar xzf ./tsung-1.7.0.tar.gz \
    && cd tsung-1.7.0 \
    && ./configure \
    && make \
    && make install \
    && rm -rf /tmp/tsung/*

EXPOSE 8091
EXPOSE 8090

CMD ["tsung", "tsung-recorder"]
