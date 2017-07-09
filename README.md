
## Elasticsearch Cluster

Start the elasticsearch:

```bash
$ docker-compose up -d
```

Check the cluster. By default, the default username is `elastic` and password is `changeme`.

```bash
$ curl -u elastic http://localhost:9200/_cat/health
```

Scale elasticsearch by creating two additional nodes

```bash
$ docker-compose up -d --scale es-nodes=2
```


```bash
# Plugin no longer works in ES5
$ open http://localhost:9200/_plugin/head/

# Open the elastichsearch-head with auth
$ open http://localhost:9100/?auth_user=elastic&auth_password=changeme
```