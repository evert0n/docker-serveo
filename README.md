# docker-serveo

Open a local tunnel with [serveo.net](https://serveo.net/)

### Usage
```
docker run --rm -ti \
  -e LOCAL_HOST=$(ifconfig | grep 'inet ' | grep -v '127.0.0.1' | head -n1 | awk '{print $2}' | cut -d: -f2) \
  -e LOCAL_PORT=3000 \
  -e REMOTE_HOST=my-test-subdomain \
  -e REMOTE_PORT=3333\
  evert0n/serveo
  
```

Then open your browser at http://my-test-subdomain.serveo.net:3333

### Alternatives

- https://ngrok.com/
- https://github.com/fatedier/frp
