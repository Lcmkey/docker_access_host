# docker_access_host

## How to check

Prepare a target.

```bash
# Start nginx as a target running on host
docker run -p 8088:80 --rm nginx

# You can see 8888 working on the host
curl localhost:8088
```

Let's access it from a container.

```bash
# Build
docker build -t docker-access-host:demo .

# Run. You should be able to see nginx result & hosts file
docker run --rm docker-access-host:demo

# It has host.docker.internal only when the host is Linux
```