FROM tomcat:8-jdk8-corretto
MAINTAINER 0x0keeper@gmail.com

ENV WAR_URL http://vulapps.xuanbo.cc/s/struts2/struts2/S2-008.war

WORKDIR /tmp

RUN set -ex \
    && rm -rf /usr/local/tomcat/webapps/* \
    && chmod a+x /usr/local/tomcat/bin/*.sh \
    && wget -qO /usr/local/tomcat/webapps/ROOT.war $WAR_URL

EXPOSE 8080
CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]
