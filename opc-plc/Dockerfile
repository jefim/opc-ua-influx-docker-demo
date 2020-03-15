FROM mcr.microsoft.com/iotedge/opc-plc:1.0
COPY entrypoint.sh /entrypoint.sh
RUN chmod a+x /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]