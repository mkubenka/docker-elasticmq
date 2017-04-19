# ElasticMQ

> Inpired by: https://github.com/s12v/elasticmq-docker

Docker image for [ElasticMQ](https://github.com/adamw/elasticmq) (fake SQS) with temprorary fix for [issue #102](https://github.com/adamw/elasticmq/issues/102).

JAR builded from https://github.com/mkubenka/elasticmq/tree/fix/102-deadletter-queue-dependency.

## Usage

```bash
docker run --rm -d -p 9324:9324 mkubenka/elasticmq
```

Custom config `elasticmq.conf` can be mounted to `/etc/elasticmq/`:
```
docker run--rm -d -p 9324:9324 -v "$PWD:/etc/elasticmq" mkubenka/elasticmq
```
