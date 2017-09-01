FROM centos
MAINTAINER henry yang


#当前目录下必须有tomcat7.tar.gz jdk8.tar.gz (解压后的名字必须相同 如： tomcat7,jdk8)
#jdk-1.8.0_linux64.tar.gz 解压后的名字可能是 jdk-1.8.0
# 如果是可以解压的文件 docker自动帮忙解压
ADD tomcat7.tar.gz /usr/local/src
ADD jdk8.tar.gz  /usr/local/src


# 相当于cd
WORKDIR /usr/local/src


ENV JAVA_HOME /usr/local/src/jdk8
ENV PATH /usr/local/src/jdk8/bin/:$PATH

RUN ln -s /usr/local/src/tomcat7/bin/catalina.sh /usr/local/bin/catalina.sh

EXPOSE 8080

ENTRYPOINT ["catalina.sh", "run" ]

