FROM ubuntu:22.10

RUN apt update && apt -y install ca-certificates curl net-tools gnupg && \
    mkdir -p /dev/net && \
    mknod /dev/net/tun c 10 200 && \
    curl -O https://raw.githubusercontent.com/angristan/openvpn-install/master/openvpn-install.sh && \
    chmod +x openvpn-install.sh && \
    AUTO_INSTALL=y ./openvpn-install.sh && \
    rm -f ./openvpn-install.sh
