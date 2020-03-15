#https://github.com/coussej/node-opcua-logger/releases/download/v2.0.0-alpha/influx-opcua-logger_v2.0.0-alpha_linux-x64
FROM alpine:3.11
RUN apk add --no-cache wget
RUN mkdir /app
RUN wget https://github.com/coussej/node-opcua-logger/releases/download/v2.0.0-alpha/influx-opcua-logger_v2.0.0-alpha_linux-x64 --output-document=/app/opc_to_influx
RUN chmod a+rwx /app/opc_to_influx
COPY config.toml /app/config.toml
COPY entrypoint.sh /app/entrypoint.sh
RUN chmod a+x /app/entrypoint.sh
RUN ls -la /app
ENTRYPOINT ["/app/entrypoint.sh"]