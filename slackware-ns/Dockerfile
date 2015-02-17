#This is a comment
FROM vbatts/slackware:latest
MAINTAINER Mathieu Bouillaguet <mathieu.bouillaguet@gmail.com>
RUN slackpkg update
RUN slackpkg -default_answer=y -batch=on install libxml2 bind
RUN chmod +x /etc/rc.d/rc.bind
EXPOSE 53
VOLUME ["/var/named/"]
ENTRYPOINT ["sh","-c","/usr/sbin/named -f"]

