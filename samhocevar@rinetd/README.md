config path:/etc/rinetd.conf

Docker-compose Example
```
version: '3'
services:
  Port-forward:
    image: acacia3/rinetd
    restart: unless-stopped
    container_name: rinetd
    volumes:
      - /EXAMPLE_PATH/rinetd.conf:/etc/rinetd.conf:ro
    network_mode: "host"
```
