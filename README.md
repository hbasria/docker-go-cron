# docker-go-cron-python

## Usage

Docker:

```sh
docker run -it --rm -p 8080:8080 -e SCHEDULE="@every 1m" hbasria/docker-go-cron-python:3.10-alpine
```

Docker Compose:

```yaml
version: '2'
services:
    go-cron-python:
        image: hbasria/docker-go-cron-python:3.10-alpin
        restart: always
        volumes:
            - /path/to/app:/app
        environment:
            - SCHEDULE=@daily
            - HEALTHCHECK_PORT=8080
```

### Environment Variables

| env variable | description |
|--|--|
| SCHEDULE | [Cron-schedule](http://godoc.org/github.com/robfig/cron#hdr-Predefined_schedules) specifying the interval between postgres backups. Defaults to `@daily`. |
