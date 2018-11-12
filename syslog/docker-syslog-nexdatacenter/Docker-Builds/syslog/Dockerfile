#
# Created : Dwiyan Galuh W
#
# dwiyan.wijatmiko@wajatmaka.com
#
# Maintenance : Dwiyan Galuh


FROM centos:7

MAINTAINER Dwiyan Galuh W

LABEL org.label-schema.person = "Dwiyan" \
      org.label-schema.name = "Syslog-NG" \
      org.label-schema.version = "3.6.XX" \
      org.label-schema.build-date = "2018-08-29"

RUN yum install -y epel-release && yum install -y syslog-ng net-tools
RUN sed -i 's/system()/# system()/g' /etc/syslog-ng/syslog-ng.conf
RUN echo '@include "/etc/syslog-ng/conf.d/networks/*.conf"' >> /etc/syslog-ng/syslog-ng.conf
RUN echo '@include "/etc/syslog-ng/conf.d/os/*.conf"' >> /etc/syslog-ng/syslog-ng.conf

VOLUME ["/log/config/conf.d/networks",  "/etc/syslog-ng/conf.d/networks"]
VOLUME ["/log/config/conf.d/os",  "/etc/syslog-ng/conf.d/os"]

EXPOSE 514:514/udp
EXPOSE 5140:5140/udp
EXPOSE 5141:5141/udp
EXPOSE 5142:5142/udp
EXPOSE 5143:5143/udp
#EXPOSE 5144:5144/udp
#EXPOSE 5145:5145/udp
#EXPOSE 5146:5146/udp
#EXPOSE 5147:5147/udp
#EXPOSE 5148:5148/udp
#EXPOSE 5149:5149/udp
#EXPOSE 5150:5150/udp


ENTRYPOINT ["/usr/sbin/syslog-ng","--no-caps","-F"]
