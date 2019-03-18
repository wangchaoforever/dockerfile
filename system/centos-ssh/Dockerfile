# Docker for CentOS

#Base image

FROM centos

#Who

MAINTAINER wangchao xxx@qq.com

#EPEL

RUN rpm -ivh http://mirrors.aliyun.com/epel/epel-release-latest-7.noarch.rpm

#Base pkg

RUN yum install -y openssh-clients openssl-devel openssh-server wget mysql-devel supervisor git redis tree net-tools sudo psmisc && yum clean all

# For SSHD

RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key

RUN ssh-keygen -t ecdsa -f /etc/ssh/ssh_host_ecdsa_key

RUN ssh-keygen -A -t dsa -f /etc/ssh/ssh_host_dsa_key

# Set root password

RUN echo "root:wangchao123" | chpasswd

#Supervisord config

ADD supervisord.conf /etc/supervisord.conf

ADD sshd.ini /etc/supervisord.d/sshd.ini

# Outside Port

EXPOSE 22

#supervisord start

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf"]

