FROM openjdk:8-jre-slim-buster

WORKDIR /home

COPY duke-core-1.3-SNAPSHOT.jar duke-core-1.3-SNAPSHOT.jar
COPY restaurants_new.nt  restaurants_new.nt
COPY config.xml config.xml
COPY entrypoint.sh /usr/local/bin/entrypoint
RUN chmod +x /usr/local/bin/entrypoint

#ENTRYPOINT [ "/bin/bash" ]
ENTRYPOINT [ "entrypoint" ]
#CMD ["java","-jar","duke-core-1.3-SNAPSHOT.jar"] 