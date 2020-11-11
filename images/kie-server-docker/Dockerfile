# podman build --rm -t quay.io/rhtgptetraining/rhpam-ks-apd:7.9 .
# podman push quay.io/rhtgptetraining/rhpam-ks-apd:7.9

FROM registry.redhat.io/rhpam-7/rhpam-kieserver-rhel8:7.9.0-7

# web services
##  Source code:   https://github.com/gpe-mw-training/advanced-process-development-labs-etc
##  After building, copy the two web artifacts into this same directory where the Dockerfile exists 
COPY ./flight-service-1.0.war /opt/eap/standalone/deployments/
COPY ./hotel-service-1.0.war /opt/eap/standalone/deployments/

COPY ./user-info.properties /home/jboss/data/

USER root
RUN chown jboss:jboss -R /home/jboss
RUN chmod -R 777 /home/jboss
RUN /opt/eap/bin/add-user.sh -a -u 'user1' -p 'bpms' -g 'user,kie-server,rest-task,rest-query,agent'
RUN /opt/eap/bin/add-user.sh -a -u 'jboss' -p 'bpms' -g 'admin,analyst,user,kie-server,rest-all'
RUN /opt/eap/bin/add-user.sh -a -u 'busadmin' -p 'bpms' -g 'Administrators,analyst,user,kie-server,rest-all'
RUN /opt/eap/bin/add-user.sh -a -u 'user10' -p 'bpms' -g 'user,group1,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user11' -p 'bpms' -g 'user,group1,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user20' -p 'bpms' -g 'user,group2,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user21' -p 'bpms' -g 'user,group2,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user30' -p 'bpms' -g 'user,group3,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user31' -p 'bpms' -g 'user,group3,kie-server,rest-task,rest-query'
