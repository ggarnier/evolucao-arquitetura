<img src="static/docker.png" style="width: 600px" />

- Setup do ambiente local muito mais simples
- Garante um ambiente igual para qualquer máquina
- Isolamento de containers

```bash
docker run --name redis -d redis
docker run --name mongodb -d mongo:2.4 mongod
docker run --name globosatplay -p 3010:3010 -v "$(pwd)":/app \
    --link mongodb:mongodb --link redis:redis globosatplay
```
