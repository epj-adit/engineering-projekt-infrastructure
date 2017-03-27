
## Installation nginx

```bash
docker pull fabianhauser/nginx-dehydrated
systemctl link `pwd`/services/nginx.service
```

## TODO: Cron update?

## Installation engineering-projekt-client

```bash
docker pull fabianhauser/engineering-projekt-client
systemctl link `pwd`/services/engineering-projekt-client.service
```

### Dehydrated

```bash
systemctl link `pwd`/services/nginx-dehydrated.service
systemctl link `pwd`/services/nginx-dehydrated.timer
systemctl link `pwd`/services/status-email-root@.service

/usr/bin/docker exec -ti nginx dehydrated --register --accept-terms
```


## TODO: Rollator

TODO

## Installation engineering-projekt-server

TODO
