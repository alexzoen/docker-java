FROM centos:7
WORKDIR /usr/bin/mvn
WORKDIR /usr/local/jdk-17
COPY apache-maven-3.6.3 /usr/bin/mvn
COPY jdk-17.0.7 /usr/local/jdk-17
ENV MAVEN_HOME=/usr/bin/mvn
ENV JAVA_HOME=/usr/local/jdk-17
ENV PATH=$MAVEN_HOME/bin:$JAVA_HOME/bin:$PATH
RUN yum -y install kde-l10n-Chinese && yum -y reinstall glibc-common
RUN localedef -c -f UTF-8 -i zh_CN zh_CN.utf8
RUN echo "export LC_ALL=zh_CN.utf8" >> /etc/profile && source /etc/profile
ENV LANG en_US.utf8
