FROM muccg/openstackbase:kilo
MAINTAINER https://github.com/muccg/

RUN apt-get -qqy update && apt-get install -y --no-install-recommends \
  mysql-client \
  python-iniparse \
  python-memcache \
  python-mysqldb \
  python-cinderclient \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY openstack-config /
COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]

CMD ["/bin/sh"]
