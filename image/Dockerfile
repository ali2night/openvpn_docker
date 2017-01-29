FROM debian:latest

# Install openvpn
RUN apt-get update && apt-get install -y openvpn supervisor vim iptables easy-rsa


# Copy rootfs
COPY rootfs /

# Fix permissions
RUN chmod +x /usr/local/bin/start.sh
# Copy easy-rsa examples
RUN mkdir /etc/openvpn/easy-rsa && cp -R /usr/share/easy-rsa/* /etc/openvpn/easy-rsa
WORKDIR /etc/openvpn

#CMD ["start.sh"]
