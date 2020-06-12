Usage:

```docker
docker build -f Dockerfile.dev -t fernandodr19/react:latest .
docker run -it -p 8080:3000 fernandodr19/react (Dockerfile.dev)
docker run -it -p 8080:80 fernandodr19/react (Dockerfile ngnix port is 80)
```

or

```docker
docker-compose up --build
```






Hot relead using volumes (-v (volumes) creates a reference instead of a copy of files, this way we can work with hot reload):
```docker
docker run -p 8080:3000 -v /app/node_modules -v $(pwd):/app fernandodr19/react-app
```

Note:
### port mappint outsideContainer:insideContainer
