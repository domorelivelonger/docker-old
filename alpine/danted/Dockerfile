
FROM alpine

RUN echo -e "http://nl.alpinelinux.org/alpine/v3.5/main\nhttp://nl.alpinelinux.org/alpine/v3.5/community" > /etc/apk/repositories
RUN echo "http://nl.alpinelinux.org/alpine/edge/testing/" >> /etc/apk/repositories

RUN apk update && apk add --no-cache dante-server

ARG user=x
ARG password=x

ENV PROXY_USER $user
ENV PROXY_PASSWORD $password

RUN adduser -S -H ${PROXY_USER} \
    && echo "${PROXY_USER}:${PROXY_PASSWORD}" | chpasswd

ADD sockd.conf /etc/sockd.conf

EXPOSE 1080

CMD ["sockd", "-f", "/etc/sockd.conf"]`
