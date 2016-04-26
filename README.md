# inventory-solr

## Build on local / dev instance

```bash
$ docker build -t gsa/inventory-solr .
$ docker run -d -p 8983:8983 --name solr gsa/inventory-solr
```

Check your browser for http://localhost:8983/solr (replace `localhost` with host name of your VM if needed)
