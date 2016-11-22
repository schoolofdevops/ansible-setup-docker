FROM centos:6
MAINTAINER InitCron
LABEL env=des
RUN yum -y install openssh-server shadow-utils
RUN echo -e "service sshd start && service sshd stop && echo \"root:123456\" | chpasswd && /usr/sbin/sshd -D" > /bootstrap.sh
EXPOSE 22
CMD ["/bin/bash","/bootstrap.sh"]
