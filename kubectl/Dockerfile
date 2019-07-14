FROM alpine:3.10.1

RUN apk --no-cache add \
        git=2.22.0-r0 \
        nano=4.3-r0 \
        vim=8.1.1365-r0 \
        curl=7.65.1-r0

RUN rm -rf /var/cache/apk/*

RUN curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl" > kubectl \
    && mv kubectl /usr/bin/ \
    && chmod +x /usr/bin/kubectl

RUN mkdir /app /root/.kube

WORKDIR /app
