# Docker for CentOS

#Base image

FROM wangchao/centos-ssh

#Who

MAINTAINER wangchao xxx@qq.com

#Base pkg

RUN yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel && yum clean all

# JAVA_HOME

ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk

# Tomcat

ADD apache-tomcat-8.5.38.tar.gz /usr/local/

RUN ln -s /usr/local/apache-tomcat-8.5.38 /usr/local/tomcat

ADD tomcat.ini /etc/supervisord.d/tomcat.ini

ENV TOMCAT_HOME /usr/local/tomcat

# Outside Port

EXPOSE 22 8080

#supervisord start

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf"]
