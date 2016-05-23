#Dockerized Mule 3.7.0 CE
#Version 3.7.0 CE
#Adapted from guide at https://blog.codecentric.de/en/2014/10/dockerizing-mule-esb-enterprise/

FROM 		java:7
MAINTAINER 	Mike Moore <moore.mike@gmail.com>

#Mule install from Host
COPY 		./mule-standalone-3.7.0.zip /opt/
WORKDIR 	/opt
RUN		unzip /opt/mule-standalone-3.7.0.zip
RUN		mv /opt/mule-standalone-3.7.0 /opt/mule
RUN 		chmod -R 755 /opt/mule/

#Expose ports

#Remote debugger port - optional
EXPOSE 5000

#MMC Agent port - optional
EXPOSE 7777

ENV	MULE_BASE /opt/mule

#Execution CMD
CMD	/opt/mule/bin/mule	
