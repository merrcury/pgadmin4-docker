# pgadmin4-docker  :whale:

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
## LICENSE
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This <span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/InteractiveResource" rel="dct:type">work</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://merrcury.github.io/" property="cc:attributionName" rel="cc:attributionURL">Himanshu Garg</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
