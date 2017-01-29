FROM debian:latest

# Install openvpn
RUN apt-get update && apt-get install -y openvpn supervisor vim


# Copy rootfs
COPY rootfs /

# Fix permissions
RUN chmod +x /usr/local/bin/start.sh

WORKDIR /etc/openvpn

CMD ["start.sh"]
