FROM node:13-alpine
RUN apk add --no-cache git openssl
RUN mkdir /app
RUN cd /app && git clone https://github.com/coussej/node-opcua-logger.git
RUN ls
RUN cd /app/node-opcua-logger && npm install --unsafe-perm
COPY config.toml /app/node-opcua-logger/config.toml
COPY entrypoint.sh /app/node-opcua-logger/entrypoint.sh
RUN chmod a+x /app/node-opcua-logger/entrypoint.sh
ENTRYPOINT ["/app/node-opcua-logger/entrypoint.sh"]
