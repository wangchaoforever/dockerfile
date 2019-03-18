# Docker for CentOS

#Base image

FROM wangchao/runtime-tomcat

#Who

MAINTAINER wangchao xxx@qq.com

# Jenkins

ADD jenkins.war /usr/local/tomcat/webapps/

# Outside Port

EXPOSE 22 8080

#supervisord start

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf"]
