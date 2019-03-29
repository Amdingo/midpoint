FROM evolveum/midpoint

MAINTAINER info@evolveum.com

ENV MP_DIR /opt/midpoint

COPY container_files/ssl_certs/ /etc/ssl/

RUN keytool -keystore /opt/midpoint/var/keystore.jceks -storetype jceks -storepass changeit -import -alias servercert -trustcacerts -file /etc/ssl/nginx.crt -noprompt

COPY container_files/mp-home/ ${MP_DIR}/var/
