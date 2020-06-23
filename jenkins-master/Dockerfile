FROM jenkins/jenkins:2.235.1-lts-alpine

USER root
RUN apk update \
    && apk add --no-cache curl docker jq tzdata \
    && rm -rf /var/cache/apk/*

ENV TZ Europe/Berlin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

USER jenkins
