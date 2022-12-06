FROM docker:dind

USER root
RUN apk update

#installing dependencies
RUN apk add curl && \
    apk add bash && \
    apk add nano && \
    apk add openssl && \
    apk add jq && \
    jq --version && \
    apk add unzip

#installing awscli
RUN apk add --no-cache aws-cli
