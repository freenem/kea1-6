FROM jrei/systemd-ubuntu

RUN apt update && apt install -y curl supervisor && curl -1sLf 'https://dl.cloudsmith.io/public/isc/kea-1-6/cfg/setup/bash.deb.sh' | bash && apt install -y isc-kea-dhcp4-server isc-kea-admin mariadb-client

COPY kea-dhcp4.conf /etc/kea/kea-dhcp4.conf
COPY my.cnf /etc/mysql/my.cnf
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
