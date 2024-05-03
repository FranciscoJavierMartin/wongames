# Won games

To create the project
```sh
docker build -f ./Dockerfile.utils -t npm-nest-utils .
docker run --rm -it -v .:/app/ npm-nest-utils nest new wongames-backend
cd wongames-backend
docker run --rm -it -v .:/app/ npm-nest-utils npm i @nestjs/graphql @nestjs/apollo @apollo/server graphql
docker run --rm -it -v .:/app/ npm-nest-utils nest g res game --no-spec
```