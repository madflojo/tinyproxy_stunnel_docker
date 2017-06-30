FROM alpine:3.6

RUN apk --no-cache add tinyproxy

ENTRYPOINT ["/usr/sbin/tinyproxy"]
CMD ["-d"]