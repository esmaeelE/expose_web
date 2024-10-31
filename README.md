# expose_web
How to expose a website to Internet from VPS.

# HINT
Using below config to remove network isolation between docker container and host not work in some old docker engins.

```
    # network_mode: "host"
```

For example in debian 12, every things seems good but we cant login to nginx proxy manager web UI with error **Not Found**
```
$ docker ps
 CONTAINER ID   IMAGE                             COMMAND                  CREATED             STATUS             PORTS                                       NAMES
3cb463d12926   jc21/nginx-proxy-manager:latest   "/init"                  About an hour ago   Up About an hour                                               next_npm-app_1
```

Use Ubuntu 24.04 instead.
```
$ lsb_release -a 
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 24.04.1 LTS
Release:        24.04
Codename:       noble
```


## Run nginx proxymanager
```
docker compose up -d
```

## Open web UI admin panel
```Public IP:81```

## Default login
```
admin@example.com
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

