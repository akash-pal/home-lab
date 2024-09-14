https://jellyfin.org/docs/general/installation/container

```
version: "3.8"

services:
  jellyfin:
    image: jellyfin/jellyfin
    container_name: jellyfin
    user: "0:0"  # Run as root (UID 0, GID 0)
    environment:
      - PUID=0            # Root user ID
      - PGID=0            # Root group ID
    ports:
      - "8096:8096"       # HTTP port
    volumes:
      - /mnt/my_ntfs_drive/jellyfin/config:/config   # Configuration storage
      - /mnt/my_ntfs_drive/jellyfin/cache:/cache     # Cache storage
      - /mnt/my_ntfs_drive/jellyfin/media:/media     # Media storage
    restart: unless-stopped

```
