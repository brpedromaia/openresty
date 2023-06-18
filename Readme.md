# Openresty Playground


## To Run The Openresty Playground:
```shell
docker-compose up --build -d
```


## To Stop The Openresty Playground:
```shell
docker-compose down
```

## To add a new service
Create new service on /usr/local/openresty/nginx/service/ folder
e.g. http-echo.conf:
```
location /apps {
    proxy_pass http://http_echo:5678;
    include /usr/local/openresty/nginx/conf/proxy.conf;
}
```

the existing configuration are inside /usr/local/openresty/nginx/conf

## SSL Certificates
to auto generate the ssl certs for local stack, make the env var PLAYGROUND_PUBLIC_DOMAIN_LOCAL_SSL_GENERATION=yes
e.g.:
```
PLAYGROUND_PUBLIC_DOMAIN_LOCAL_SSL_GENERATION=yes
```

## Endpoints:

- Openresty Welcome Page: https://playground.rec.la
- Http echo webapp test:  https://playground.rec.la/apps/http_echo
