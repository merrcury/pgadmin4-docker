# pgadmin4-docker

+ For running PGADMIN4 Docker with automated NGNIX Reverse Proxy and Let's Encrypt certificate. 
  + Use `docker-compose.ngnix.yml`. 
  + Edit & Change Variables `VIRTUAL_HOST`, `LETSENCRYPT_HOST`, `LETSENCRYPT_EMAIL`, `PGADMIN_DEFAULT_EMAIL` and `PGADMIN_DEFAULT_PASSWORD`


+ For running a PGADMIN4 Docker as TLS Secured Container. (Self-Managed)
  + Use `docker-compose.selfmanaged.yml`. 
  + Edit & Change Variables `PGADMIN_DEFAULT_EMAIL` and `PGADMIN_DEFAULT_PASSWORD`
  + Create Self-Signed Certificate & Key using OpenSSL and edit path in compose file.
  
+ For Non-TLS PGADMIN4 Docker:
  ``` bash 
  docker run -p 80:80 \
      -e 'PGADMIN_DEFAULT_EMAIL=john.doe@domain.com' \
      -e 'PGADMIN_DEFAULT_PASSWORD=SuperSecret' \
      -d dpage/pgadmin4
  ```
