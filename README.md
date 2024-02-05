# roadrunner-docker-skeleton
A local docker environment skeleton for [RoadRunner](https://github.com/roadrunner-server/roadrunner), the PHP application server written in golang.

HTTP Server and PHP Workers are enabled by default.


## Requirements
- Bash
- Docker Compose

## Install

### via Git
```
git clone https://github.com/GodlikeBasic/roadrunner-docker-skeleton.git your_app
cd your_app

./task create
```

## Commands

### Start the container

```
./task start

# with rebuilding image
# ./task start --build
```

and access http://localhost:8080

### Stop the container

```
./task stop
```

### Login into the container
```
./task login
```

### Show container log
```
./task logs
```

### Execute RoadRunner commands

```
./task rr {command}
# ex) ./task rr help
```
