FROM centos:7

# インストール済みのパッケージをアップデート＆キャッシュのクリア
RUN yum -y update && yum clean all

# yum install
RUN yum install sudo -y
RUN yum install vim -y
RUN yum install git -y
RUN yum install net-tools -y
RUN yum install wget -y

# java install
RUN yum -y install java-1.8.0-openjdk.x86_64
RUN yum -y install java-1.8.0-openjdk-devel.x86_64

# scala install
RUN cd /usr/local/src/ && wget https://downloads.lightbend.com/scala/2.12.6/scala-2.12.6.tgz
RUN cd /usr/local/src/ && tar xvzf scala-2.12.6.tgz
RUN cd /usr/local/src/ && mv scala-2.12.6 /usr/local/scala

# go install
RUN cd /usr/local/src/ && wget https://dl.google.com/go/go1.10.2.linux-amd64.tar.gz
RUN cd /usr/local/src/ && tar -C /usr/local -xzf go1.10.2.linux-amd64.tar.gz

# switch
USER root
