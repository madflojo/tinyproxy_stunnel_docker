FROM alpine:edge

RUN apk --no-cache add stunnel

RUN mkdir /etc/stunnel/certs/

ENTRYPOINT ["/usr/bin/stunnel"]
CMD ["/etc/stunnel/stunnel.conf"]
