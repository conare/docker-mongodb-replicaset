FROM mongo:latest
MAINTAINER Ronald Maduka
ENV MONGO_DIR /opt/mongor
ENV REPLICA_NAME "ReplicaSet"
ENV TRY_TIMES 5
ENV CONFIG_DIR /var/config
ENV REPLICA_LABEL "mongo.replicaset.db"
ENV LOG_FILE /var/log/mongodb.log
ENV SOURCE "cloud"
RUN apt-get update && apt-get install -y python python-pip
RUN pip install docker-cloud
COPY scripts $MONGO_DIR
LABEL $REPLICA_LABEL=$REPLICA_NAME
#RUN bash $MONGO_DIR/init.sh
ENTRYPOINT bash $MONGO_DIR/main.sh

