# inventory-solr

## Build on local / dev instance

```bash
$ docker build -t gsa/inventory-solr .
$ docker run -d -p 8983:8983 --name solr gsa/inventory-solr
```

* In your browser, you must be able to open http://localhost:8983/solr (replace `localhost` with host name of your VM if needed)
* Configure your CKAN .ini file to use your new SOLR instance (replace `localhost` with host name of your VM if needed)
```
solr_url = http://localhost:8983/solr/ckan
```