# m2i-tp5

## Provided files

### deployment
In this file we have all the YAML deployment files in the kubernetes cluster.
This folder contains deployment file for:
- elasticsearch
- kibana
- filebeat
- nginx

### service
In this file we have all the services YAML files to be deployed in the kubernetes cluster.
This folder contains service files for:
- elasticsearch
- kibana
- nginx

### Config_files
filebeat_config.yml 
This filebeat configuration file is for:
- Collecting logs of docker containers in /var/lib/docker/containers
- Send logs to logstach pipeline into port 5044
- Enhance logs with kubernetes metadata

pipeline_nginx.conf
This logstach pipeline
- Récupère les logs au format Common Log Format de Nginx
- Parse les logs dans un format structuré 
- Extrait la date des logs
- Indexe les logs dans Elasticsearch dans un index quotidien dédié à Nginx

index_kibana.json: Allow Kibana to index all the correponding index to nginx-logs-*

filter_kibanajson: show logs of the namespace default in kibana

## Pre-requisite
- Clone the git repository from github : https://github.com/caiimy/m2i-tp5.git
- A kubernetes cluster in production

