FROM mariadb:10.1

RUN apt update && apt install -y curl && curl -1sLf 'https://dl.cloudsmith.io/public/isc/kea-1-6/cfg/setup/bash.deb.sh' | bash && apt install -y isc-kea-admin

COPY init.sh /docker-entrypoint-initdb.d/
