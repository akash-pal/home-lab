Docker Compose

```
version: '3.8'
volumes:
  nextcloud_aio_mastercontainer:
    name: nextcloud_aio_mastercontainer
services:
  nextcloud:
    image: 'nextcloud/all-in-one:latest'
    restart: unless-stopped
    container_name: nextcloud-aio-mastercontainer
    volumes:
      - 'nextcloud_aio_mastercontainer:/mnt/docker-aio-config'
      - '/var/run/docker.sock:/var/run/docker.sock:ro'
    ports:
      - '8084:8080'
    environment:
      - APACHE_PORT=11000
      - APACHE_DISABLE_REWRITE_IP=1
      - NEXTCLOUD_TRUSTED_DOMAINS=nextcloud.palsky.duckdns.org 192.168.1.10
      - TRUSTED_PROXIES=192.168.1.10
      - NEXTCLOUD_DATADIR=/mnt/my_ntfs_drive/ncdata

```
