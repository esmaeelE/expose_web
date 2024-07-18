# expose_web
How to expose a website to Internet from VPS.

## Run nginx proxymanager
```
docker compose up -d
```

## Open web UI admin panel
```Public IP:81```

## Default login
```
admin@exmaple.com
changeme
```
## Example

### Redirect traffic to docker container
```
172.17.0.1:8080
```

### Redirect traffic to localhost service
```
127.0.0.1:8080
```

