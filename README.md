# docker-serveo

Open a local tunnel with serveo.net


### Usage
```
docker run --rm -ti \
  -e LOCAL_HOST=$PRIVATE_IP \
  -e LOCAL_PORT=3000 \
  -e REMOTE_HOST=my-test-subdomain \
  -e REMOTE_PORT=3333\
  evert0n/serveo
  
```

Then open your browser at http://my-test-subdomain.serveo.net:3333