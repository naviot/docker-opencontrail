FROM michaelhenkel/nova:liberty
MAINTAINER https://hub.docker.com/r/michaelhenkel

#RUN apt-get -qqy update && apt-get install -y --no-install-recommends \
#  nova-scheduler \
#  && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
COPY entrypoint.sh /

CMD ["/usr/bin/python","/usr/bin/nova-scheduler"]

LABEL net.juniper.openstack=nova
LABEL net.juniper.node=controller
