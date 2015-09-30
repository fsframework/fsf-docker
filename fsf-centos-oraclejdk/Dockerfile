FROM centos:7
MAINTAINER FSFramework <5sframework@gmail.com>

RUN yum -y install wget tar unzip \
    && wget -P /opt/ --no-check-certificate --no-cookies \
        --header "Cookie: oraclelicense=accept-securebackup-cookie" \
        http://download.oracle.com/otn-pub/java/jdk/8u60-b27/jdk-8u60-linux-x64.rpm \
    && yum -y install /opt/jdk-8u60-linux-x64.rpm \
    && rm /opt/jdk-8u60-linux-x64.rpm \
    && yum -y clean all

ENV JAVA_HOME /usr/java/default
ENV PATH $JAVA_HOME/bin:$PATH
