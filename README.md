# Won games

To create the project

```sh
docker build -f ./Dockerfile.utils -t npm-nest-utils .
docker run --rm -it -v .:/app/ npm-nest-utils nest new wongames-backend
cd wongames-backend
docker run --rm -it -v .:/app/ npm-nest-utils npm i @nestjs/graphql @nestjs/apollo @apollo/server graphql
docker run --rm -it -v .:/app/ npm-nest-utils nest g res game --no-spec
docker-compose -f docker-compose.dev.yml  up --build
```

## Development setup

### Requirements

- Docker installed and running. Docker desktop is recommended.
- Git installed and configured.
- A code editor of your choice.

### Steps

1. Clone repo

```sh
git clone https://github.com/FranciscoJavierMartin/wongames.git
```

2. Get the submodules

```sh
git submodule update --init --recursive
```

3. Create a new file _.env_ at the root project. Copy the content of _.env.template_ inside the _.env_ file and replace with your own values.
4. Run docker-compose for development.

```sh
docker-compose -f docker-compose.dev.yml up --build
```
Now your project is ready to coding.
