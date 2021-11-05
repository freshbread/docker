FROM tomcat:8.5.61-jdk8-openjdk

ENV IR4_HOME /usr/local/mariner4

ARG M4_VER=4.3.3.2

RUN apt-get update -y 
RUN apt-get install vim -y
#RUN mkdir /usr/local/mariner4

#COPY ./files/dq-mariner4-$M4_VER.tar.gz /usr/local/mariner4

WORKDIR /usr/local/mariner4
#RUN tar -zxvf dq-mariner4-$M4_VER.tar.gz
#RUN rm dq-mariner4-$M4_VER.tar.gz

COPY ./files/server.xml /usr/local/tomcat/conf/
#COPY ./files/ir.rdbms.properties /usr/local/mariner4/rdbms/
#COPY ./files/common.jsp /usr/local/mariner4/webManager/m4/common/

EXPOSE 5001
EXPOSE 5555
EXPOSE 8080

ENTRYPOINT ["catalina.sh", "run"]