# inventory-solr

## Build on local / dev instance

```bash
$ docker build -t gsa/inventory-solr .
$ docker run -d -p 8983:8983 --name solr gsa/inventory-solr
```

* In your browser, you must be able to open (replace `localhost` with host name of your VM if needed): http://localhost:8983/solr
* Configure your CKAN .ini file to use your new SOLR instance (replace `localhost` with host name of your VM if needed)
```
solr_url = http://localhost:8983/solr/ckan
```
* If you already have data in your CKAN, you can rebuild SOLR data: http://docs.ckan.org/en/latest/maintaining/paster.html#search-index-rebuild-search-index
