# Apache + Kafka + Zookeeper + Prometheus + Grafana + Docker
A docker compose example to deploy multiple brokers in a VM cluster with Prometheus and Grafana enabled for Kafka brokers monitoring

## Commands to run the docker files

```
sudo docker run -p 9090:9090 --name=prometheus --restart unless-stopped -v /opt/prometheus:/etc/prometheus prom/prometheus

docker run -p 3000:3000 --name=grafana --restart unless-stopped -e GF_AUTH_ANONYMOUS_ENABLED=true -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin -v grafana-storage:/var/lib/grafana grafana/grafana
```

Add a Prometheus Data Source and a Dashboard in Grafana UI
