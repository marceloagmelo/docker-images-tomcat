FROM marceloagmelo/java:7

MAINTAINER Marcelo Melo <marceloagmelo@gmail.com>

ENV TOMCAT_VER=apache-tomcat-7.0.69
ENV BASE=/opt
ENV TOMCAT_HOME=${BASE}/${TOMCAT_VER}

RUN (mkdir ${TOMCAT_HOME})

# install tomcat
ADD ${TOMCAT_VER}/ ${TOMCAT_HOME}/

# tomcat users
ADD tomcat-users.xml ${TOMCAT_HOME}/conf/

WORKDIR ${TOMCAT_HOME}/

RUN (sudo chown root:root ${TOMCAT_HOME})

EXPOSE 8080
CMD ["/opt/apache-tomcat-7.0.69/bin/catalina.sh", "run"]
