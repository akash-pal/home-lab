[Guide](https://wiki.opensourceisawesome.com/books/docker-management/page/installing-portainer-ce-and-or-portainer-agent)

1. Setup a Portainer data volume.
```
docker volume create portainer_data
```

2. Install Portainer CE
```
docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```
