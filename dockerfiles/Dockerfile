
# Usar as seguintes configurações no Dockerfile

ARG PUID=1000
ENV PUID ${PUID}
ARG PGID=1000
ENV PGID ${PGID}

RUN groupadd -g ${PGID} adminuser
RUN useradd -u ${PUID} -g adminuser -G www-data -m adminuser
RUN usermod -p "*" adminuser -s /bin/bash
RUN usermod -a -G www-data adminuser

WORKDIR /usr/share/nginx

COPY www.conf /etc/php/8.0/fpm/pool.d/