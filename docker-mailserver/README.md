###
Para configurarlo:
Primero se debe ejecutar dentro de la carpeta docker-mailserver
```
docker run --rm -it \                                                            
  -v "${PWD}/dms/certbot/certs/:/etc/letsencrypt/" \
  -v "${PWD}/dms/certbot/logs/:/var/log/letsencrypt/" \
  -p 80:80 \
  certbot/certbot certonly --standalone -d ventruetechnologies.com

```
```
docker run --rm -it \                                                            
  -v "${PWD}/dms/certbot/certs/:/etc/letsencrypt/" \
  -v "${PWD}/dms/certbot/logs/:/var/log/letsencrypt/" \
  -p 80:80 \
  certbot/certbot certonly --standalone -d mail.ventruetechnologies.com

```