# docker for serveo.net

<https://serveo.net> is an alternative for ngrok.

## Usage

1. write a `docker-compose.yml` file.

```yml
version: '2'

services:
  serveo:
    image: trumpi/serveo:latest
    tty: true
    stdin_open: true
    # see https://serveo.net/ for more options
    command: "autossh -M 0 -R 80:nginx:80 -o \"StrictHostKeyChecking no\" serveo.net"
  nginx:
    image: nginx:latest
```

2. use `docker-compose up -d` to start container.

3. you need to use `docker-compose logs serveo` to see your new URL.

## LICENSE

MIT License
