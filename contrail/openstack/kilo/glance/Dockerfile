FROM muccg/openstackbase:kilo
MAINTAINER https://github.com/muccg/

RUN apt-get -qqy update && apt-get install -y --no-install-recommends \
  mysql-client \
  python-iniparse \
  python-memcache \
  python-mysqldb \
  python-ceph \
  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY openstack-config /
LABEL net.juniper.openstack=glance
LABEL net.juniper.node=controller

CMD ["/bin/sh"]
