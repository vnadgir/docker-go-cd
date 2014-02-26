FROM centos
MAINTAINER Vaishakh Nadgir <vnadgir@gmail.com>
#ADD go-agent-13.4.1-18342.noarch.rpm /tmp/go-agent.rpm
ADD http://download01.thoughtworks.com/go/13.4.1/ga/go-agent-13.4.1-18342.noarch.rpm /tmp/go-agent.rpm
RUN yum install -y java-1.7.0-openjdk.x86_64
RUN yum localinstall -y /tmp/go-agent.rpm
ENV JAVA_HOME /usr/lib/jvm/java-1.7.0-openjdk-1.7.0.51.x86_64/jre
RUN echo "JAVA_HOME=$JAVA_HOME" >> /etc/default/go-agent
CMD service go-agent start
