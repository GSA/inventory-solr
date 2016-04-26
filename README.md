# inventory-solr

## Build on local / dev instance

Use one of two ways to run a container:

1) To run a build directly from Docker hub, run
```bash
$ docker run -d -p 8983:8983 --name solr datagov/inventory-solr
```
2) Build an image from Dockerfile from this repo
```bash
$ git clone https://github.com/GSA/inventory-solr.git
$ docker build -t datagov/inventory-solr .
$ docker run -d -p 8983:8983 --name solr datagov/inventory-solr
```

In your browser, you must be able to open (replace `localhost` with host name of your VM if needed): 
[http://localhost:8983/solr](http://localhost:8983/solr)

## CKAN config
Configure your CKAN .ini file to use your new SOLR instance (replace `localhost` with host name of your VM if needed)
```
solr_url = http://localhost:8983/solr/ckan
```

## Rebuilding SOLR index
If you already have data in your CKAN, you can rebuild SOLR data: http://docs.ckan.org/en/latest/maintaining/paster.html#search-index-rebuild-search-index
