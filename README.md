# fluentd-elasticsearch
A image setting with Elasticsearch output plugin to send event data to Elasticsearch server.

You must have a server with Elasticsearch installed and configured on port 9200.


# hands-on
Ensure that Elasticsearch is running and run the container:

```bash
docker run --rm -p 24224:24224 bortes/fluentd-elasticsearch
```


After that, just run your desired dockerized application and setting logger output. For example:

```bash
docker run --rm -p 8080:80 --log-driver=fluentd --log-opt fluentd-address=localhost:24224 nginx:alpine
```


# next steps
Enable the pipeline for Elasticsearch.


# more info
Based on [Fluentd](https://docs.fluentd.org/v1.0/articles/config-file) with [Elasticsearch plugin](https://github.com/uken/fluent-plugin-elasticsearch).

About [Docker logger](https://docs.docker.com/engine/admin/logging/overview/) output and [Logging Driver to Fluentd](https://docs.fluentd.org/v0.12/articles/docker-logging).
