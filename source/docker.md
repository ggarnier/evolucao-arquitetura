<img src="static/docker.png" />

https://www.docker.com/

- Setup do ambiente local muito mais simples
- Um container por processo

```bash
docker run --name redis -p 6379:6379 -d redis
docker run --name mongodb -p 27017:27017 -v $HOME/data/mongo:/data -d mongo:2.4 mongod --smallfiles
docker run --name globosatplay -p 3010:3010 -v "$(pwd)":/app --link mongodb:mongodb --link redis:redis globosatplay
```
