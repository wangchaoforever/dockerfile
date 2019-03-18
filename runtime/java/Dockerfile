# Docker for CentOS

#Base image

FROM wangchao/centos-ssh

#Who

MAINTAINER wangchao xxx@qq.com

#Base pkg

RUN yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel && yum clean all

# JAVA_HOME

ENV JAVA_HOME /usr/lib/jvm/java-1.8.0-openjdk

# Outside Port

EXPOSE 22

#supervisord start

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf"]
