# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.openshift.expose-services="8080:http"

label IO.K8S.DESCRIPTION="a BASIC aPACHE http sERVER CHILD IMAGE, USES onbuild" \
      IO.K8S.DISPLAY-NAME="aPACHE http sERVER" \
      IO.OPENSHIFT.EXPOSE-SERVICES="8080:HTTP" \
      IO.OPENSHIFT.TAGS="APACHE, HTTPD"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001


