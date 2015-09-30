FROM centos:centos7
MAINTAINER FSFramwwork <5sframework@gmail.com>

RUN groupadd -r postgres && useradd -r -g postgres postgres

RUN yum -y update \
	&& yum -y install wget \ 
    && wget http://yum.postgresql.org/9.4/redhat/rhel-7-x86_64/pgdg-centos94-9.4-1.noarch.rpm \
    && rpm -Uvh pgdg-centos94-9.4-1.noarch.rpm \
    && yum -y install postgresql94-server postgresql94-contrib \
    && yum clean all

RUN mkdir -p /dbms/data01 && chown -R postgres:postgres /dbms/data01
VOLUME /dbms/data01

USER postgres
ENV PATH /usr/pgsql-9.4/bin:$PATH
ENV PGDATA /dbms/data01/default


EXPOSE 5432
CMD postgres -D $PGDATA 
