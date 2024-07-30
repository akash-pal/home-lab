Docker Compose

```
services:
  heimdall:
    image: lscr.io/linuxserver/heimdall:latest
    container_name: heimdall
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Asia/Calcutta
    volumes:
      - /path/to/heimdall/config:/config
    ports:
      - 8080:80
      - 1443:443
    restart: unless-stopped

```
