FROM centos/httpd
MAINTAINER FSFramework <5sframework@gmail.com>

COPY setup/mod_jk.so /etc/httpd/modules/
COPY setup/02-modjk.conf /etc/httpd/conf.modules.d/
COPY setup/mod-jk.conf setup/workers.properties /etc/httpd/conf.d/
