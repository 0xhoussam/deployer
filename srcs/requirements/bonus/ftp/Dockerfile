FROM alpine:3.18

EXPOSE 20
EXPOSE 21
EXPOSE 30000-30100

RUN apk update

RUN apk add vsftpd

COPY ./conf/vsftpd.conf /etc/vsftpd/vsftpd.conf
COPY ./tools/entrypoint.sh /entrypoint
RUN chmod 770 /entrypoint

ENTRYPOINT [ "/entrypoint" ]

CMD ["/usr/sbin/vsftpd", "/etc/vsftpd/vsftpd.conf"]

