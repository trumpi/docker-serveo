FROM alpine:latest
LABEL maintainer="git@trumpi.co.za"

RUN apk add --no-cache openssh
RUN apk update && \
  echo "http://dl-cdn.alpinelinux.org/alpine/edge/community/" >> /etc/apk/repositories && \
  apk add --update autossh && \
  rm -rf /var/lib/apt/lists/*
CMD ["/bin/sh"]
