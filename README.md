# Redis
### Run and go Docker setup for Redis.

<br />

To start Redis on background via Docker just type:
```
docker compose up -d
```

Main parametrs can be modified via `.env` file.


Default configuration:
```
IMAGE: redis:7.0.8
CONTAINER NAME: redis
PASSWORD: admin
PORT: 6379 (default for Redis)
```

Data are persisted locally:
```
./volumes/redis/data
```

Cmd verification that all is working:
```
> docker exec -ti redis bash
> redis-cli
> AUTH <password>
ok
> keys *
(empty array)
> exit
```

Docker network:
```
redis
```