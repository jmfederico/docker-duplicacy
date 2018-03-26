FROM alpine:latest

RUN mkdir -p /srv/backup
WORKDIR /srv/backup

RUN apk --no-cache add ca-certificates openssl && \
    wget -O /usr/local/bin/duplicacy https://github.com/gilbertchen/duplicacy/releases/download/v2.1.0/duplicacy_linux_x64_2.1.0

RUN chmod u+x /usr/local/bin/duplicacy

ENTRYPOINT ["duplicacy"]

CMD ["backup"]
