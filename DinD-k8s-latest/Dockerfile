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

#installing kops
RUN curl -Lo kops https://github.com/kubernetes/kops/releases/download/$(curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64 && \
    chmod +x kops && \
    mv kops /usr/local/bin/kops && \
    kops version

#installing kubectl
RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && \
    install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl && \
    kubectl version --client



