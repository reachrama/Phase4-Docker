#FROM recapscsb/scsb-base:latest
FROM phase4-scsb-base:latest
MAINTAINER HTC ReCAP Support "recap-support@htcindia.com"

ARG TAG
ENV envTag="$TAG"
COPY shellBuild.sh /opt/
RUN cd /opt && ls -l && ./shellBuild.sh ${envTag}

ENTRYPOINT java -jar -Denvironment=$ENV /opt/Phase4-SCSB-UI.jar && bash