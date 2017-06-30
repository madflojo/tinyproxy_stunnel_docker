FROM alpine:edge

RUN apk --no-cache add openssl stunnel
  
RUN mkdir /etc/ssl/mycerts  
  
RUN openssl req -new -newkey rsa:4096 -days 24854 -nodes -x509 \
    -subj "/C=US/ST=Denial/L=Springfield/O=Dis/CN=www.example.com" \
    -keyout /etc/ssl/key.pem  -out /etc/ssl/cert.pem

ENTRYPOINT cp /etc/ssl/cert.pem /etc/ssl/mycerts/ && /usr/bin/stunnel
CMD ["/etc/stunnel/stunnel.conf"]
