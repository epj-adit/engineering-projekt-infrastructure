
## Installation nginx

```bash
docker pull fabianhauser/nginx-dehydrated
systemctl link `pwd`/services/nginx.service
systemctl start nginx.service
```

### TODO: Cron update?

## Installation engineering-projekt-client

```bash
docker pull fabianhauser/engineering-projekt-client
systemctl link `pwd`/services/engineering-projekt-client.service
systemctl start engineering-projekt-client.service
```

### Dehydrated

```bash
systemctl link `pwd`/services/nginx-dehydrated.service
systemctl link `pwd`/services/nginx-dehydrated.timer
systemctl link `pwd`/services/status-email-root@.service

/usr/bin/docker exec -ti nginx dehydrated --register --accept-terms
systemctl start nginx-dehydrated.service

```


## TODO: Rollator

TODO

## Installation engineering-projekt-server

TODO


## Sonarqube

```bash
cp sonarqube/sonarqube.env /etc/
# Replace ###POSTGRES_PASSWORD### with a random password string
systemctl link `pwd`/services/sonarqube-postgres.service
systemctl start sonarqube-postgres.service

systemctl link `pwd`/services/sonarqube.service
systemctl start sonarqube.service
```

