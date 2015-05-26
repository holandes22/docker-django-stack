FROM holandes22/base

MAINTAINER Pablo Klijnjan <pabloklijnjan@gmail.com>

CMD ["/sbin/my_init"]

RUN locale-gen en_US.UTF-8 && \
    echo 'LANG="en_US.UTF-8"' > /etc/default/locale

RUN echo "deb http://apt.postgresql.org/pub/repos/apt/ trusty-pgdg main" > /etc/apt/sources.list.d/pgdg.list && \
    apt-get update && \
    DEBIAN_FRONTEND=noninteractive \
    apt-get install -y --force-yes \
    postgresql-9.4 postgresql-client-9.4 postgresql-contrib-9.4 && \

VOLUME ["/var/log/postgresql", "/etc/postgresql"]

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

