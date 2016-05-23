#HelloProxy
#Version 1.0
#Adapted from guide at https://blog.codecentric.de/en/2014/10/dockerizing-mule-esb-enterprise/

FROM 		mule-ce:3.7.0
MAINTAINER 	Mike Moore <moore.mike@gmail.comm>

COPY		./helloproxy.zip ${MULE_BASE}/apps/

#Expose the endpoint Mule is listening on for this app
EXPOSE 8080

#Set environment variables for Registrator to pick up (SERVICE_PORT_KEY)
ENV SERVICE_8080_NAME hello-proxy
#This environment is required for Fabio URL path routing
ENV SERVICE_8080_TAGS urlprefix-/test/hello/proxy
#This is required for Consul health check
ENV SERVICE_8080_CHECK_HTTP /test/hello/proxy

RUN		chmod -R 755 ${MULE_BASE}/apps/
