###

# Para configurarlo:

1. Parar servicios que usen el puerto 80

2. generar los certificados para el dominio

```
docker run --rm -it -v "${PWD}/dms/certbot/certs/:/etc/letsencrypt/" -v "${PWD}/dms/certbot/logs/:/var/log/letsencrypt/" -p 80:80 certbot/certbot certonly --standalone -d ventruetechnologies.com

```

3.  Generar los certificados para el dominio MX

```
docker run --rm -it -v "${PWD}/dms/certbot/certs/:/etc/letsencrypt/" -v "${PWD}/dms/certbot/logs/:/var/log/letsencrypt/" -p 80:80 certbot/certbot certonly --standalone -d mail.ventruetechnologies.com

```
