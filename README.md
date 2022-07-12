# Apache + Kafka + Zookeeper + Docker
A docker compose example to deploy multiple brokers in a VM cluster

## Commands to run the docker files

```
docker compose up --build -d

docker run --name=prometheus --restart unless-stopped -v ./jmx-exporter:/etc/prometheus prom/prometheus

docker run --name=grafana --restart unless-stopped -e GF_AUTH_ANONYMOUS_ENABLED=true -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin -v grafana-storage:/var/lib/grafana grafana/grafana
```
