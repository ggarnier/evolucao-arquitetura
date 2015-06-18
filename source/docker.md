<img src="static/docker.png" />

https://www.docker.com/

- Setup do ambiente local muito mais simples
- Um container por processo

```bash
docker run --name redis -d redis
docker run --name mongodb -d mongo:2.4 mongod
docker run --name globosatplay -p 3010:3010 -v "$(pwd)":/app \
    --link mongodb:mongodb --link redis:redis globosatplay
```
