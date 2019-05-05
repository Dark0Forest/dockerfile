FROM vincentail/centos_nginx
MAINTAINER vincent (jichun.chang90@gmail.com)
#use jdk :jdk-8u211-linux-x64.tar.gz
ADD jdk-8u211-linux-x64.tar.gz /app/
WORKDIR /app
ENV JAVA_HOME=/app/jdk1.8.0_211
ENV CLASSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
ENV PATH $PATH:$JAVA_HOME/bin

RUN wget http://ftp.cuhk.edu.hk/pub/packages/apache.org/tomcat/tomcat-9/v9.0.19/bin/apache-tomcat-9.0.19.tar.gz

RUN tar -zxvf apache-tomcat-9.0.19.tar.gz
RUN rm -rf *.tar.gz

EXPOSE 80