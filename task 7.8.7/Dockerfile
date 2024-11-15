FROM alpine:3.20.3

RUN apk add wget

COPY getfile.sh /

WORKDIR /out

ENTRYPOINT ["/getfile.sh"]