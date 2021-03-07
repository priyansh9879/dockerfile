FROM priyanshmagotra/fedora-systemd

MAINTAINER "priyansh9879" <priyanshmagotra444@outlook.com>

RUN mkdir -p /var/run/sshd

RUN yum install vim wget curl net-tools ansible openssh-server openssh-clients --nogpgcheck -y && ssh-keygen -A

RUN wget https://raw.githubusercontent.com/priyansh9879/dockerfile/master/ansible/sshd_config -O /etc/ssh/sshd_config 

RUN echo "root:redhat" | chpasswd

CMD ["/usr/sbin/sshd", "-D"]
