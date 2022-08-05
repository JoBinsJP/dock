## MySql Grants:

For MySql57 `Access denied for user 'root'@'localhost'` issue:
- run following before creating database. If database already created, drop database and create
after running this command.

```sql
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'password';
```

Traefik Certificates for HTTPs

1. install [mkcert](https://github.com/FiloSottile/mkcert)
```shell
# If it's the firt install of mkcert, run
mkcert -install
```

2. Generate certificate for domain and store in certs
```shell
mkcert -cert-file traefik/certs/local-cert.pem -key-file traefik/certs/local-key.pem "localhost" "jobins-crm.localhost"
```