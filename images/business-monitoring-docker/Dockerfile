# podman build --rm -t quay.io/rhtgptetraining/rhpam-monitoring-apd:1.3 .

FROM registry.redhat.io/rhpam-7/rhpam-businesscentral-monitoring-rhel8:7.5.1-1
USER root
RUN chown jboss:jboss -R /home/jboss
RUN chmod -R 777 /home/jboss
RUN /opt/eap/bin/add-user.sh -a -u 'user1' -p 'bpms' -g 'user,kie-server,rest-task,rest-query,agent'
RUN /opt/eap/bin/add-user.sh -a -u 'jboss' -p 'bpms' -g 'admin,analyst,user,kie-server,rest-all,agent'
RUN /opt/eap/bin/add-user.sh -a -u 'busadmin' -p 'bpms' -g 'Administrators,analyst,user,kie-server,rest-all'
RUN /opt/eap/bin/add-user.sh -a -u 'user10' -p 'bpms' -g 'user,group1,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user11' -p 'bpms' -g 'user,group1,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user20' -p 'bpms' -g 'user,group2,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user21' -p 'bpms' -g 'user,group2,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user30' -p 'bpms' -g 'user,group3,kie-server,rest-task,rest-query'
RUN /opt/eap/bin/add-user.sh -a -u 'user31' -p 'bpms' -g 'user,group3,kie-server,rest-task,rest-query'
