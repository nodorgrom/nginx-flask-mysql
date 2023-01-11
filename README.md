## Deploy with docker compose
```
$ docker compose up -d
```


## Expected result
```
$ docker compose ps
NAME                          COMMAND                  SERVICE             STATUS              PORTS
nginx-flask-mysql-backend-1   "flask run"              backend             running             0.0.0.0:8000->8000/tcp
nginx-flask-mysql-db-1        "docker-entrypoint.s…"   db                  running (healthy)   3306/tcp, 33060/tcp
nginx-flask-mysql-proxy-1     "nginx -g 'daemon of…"   proxy               running             0.0.0.0:80->80/tcp
```


## Navigate to localhost
```
$ curl localhost:80
```


## Stop and remove the containers
```
$ docker compose down
```


## Restart container
```
$ docker compose restart <service>
```
