
FROM centos:7
MAINTAINER dinky
ADD flink-1.14.6-bin-scala_2.11.tgz  /root
ADD jdk-8u261-linux-x64.tar.gz  /root
ADD dinky-app.jar  /root
ARG FLINK_VERSION=1.14.6
ARG SCALA_VERSION=2.11
ENV FLINK_HOME=/root/flink-1.14.6
ENV PATH=$FLINK_HOME/bin:$PATH
ENV JAVA_HOME=/root/jdk1.8.0_261
ENV PATH=$JAVA_HOME/bin:$PATH

RUN cd $FLINK_HOME  \
       && echo "env.java.home: /root/jdk1.8.0_261" >> $FLINK_HOME/conf/flink-conf.yaml \
       && echo "FLINK_HOME=/root/flink-1.14.6" >> /etc/profile \
       && echo "PATH=$FLINK_HOME/bin:$PATH" >> /etc/profile \
       && echo "JAVA_HOME=/root/jdk1.8.0_261" >> /etc/profile \
       && echo "PATH=$JAVA_HOME/bin:$PATH" >> /etc/profile \
       && source /etc/profile

EXPOSE 8081

