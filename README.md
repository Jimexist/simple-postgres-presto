# Dockerized [PrestoDB](https://prestodb.io/)

This is is mainly for usage with CircleCI.

To run within CircleCI that has Postgres:

```sh
docker run -d --name presto1 -p 8080:8080 -h presto --add-host postgresql:$(ip addr show docker0 | grep "inet\b" | awk '{print $2}' | cut -d/ -f1) jimexist/simple-postgres-presto
```

