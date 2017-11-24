php-fpm Dockerfile

# Usage

To run container with additional php extensions use 

```
sudo docker build --build-arg phpext="pcntl pdo_mysql" 
```


# Docker-compose usage

version: '2'
services:
  fpm:
    image: fink3l/fpm:latest
    build:
      context: "https://github.com/fink3l/docker-fpm-container.git"
      args:
        phpext: "pcntl pdo_mysql"
