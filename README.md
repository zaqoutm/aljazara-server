# Server setup

## Services

- directus
- postgres
- nginx

## Folders

- `site/` website files
- `directus/` directus files
- `nginx/` configurations
- `pg_data/` postgres data
- `tls/` ssl certificates

## Run

First set the .env, example added `/env-examlpe`

```sh
docker-compose up
```

## Generate TLS letsencrypt certificate

Add .env file

```sh
EMAIL=your-email
DOMAIN=your-domain.com
CERTIFICATE_FOLDER=your-domain
```

Generate dhparam

```sh
sudo openssl dhparam -out ./dhparam/dhparam.pem 2048
```

`docker compose up`

```
#certbot-1  | Successfully received certificate.
#...
#certbot-1 exited with code 0
```

Will find new folder `tls/domain/` created contains cerificates
`conf/ data/ logs/`
