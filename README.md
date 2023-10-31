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
- Catch logs in Common Log Format of Nginx
- Parse logs in a structured format
- Extract date from logs
- Index logs from Elasticsearch in a dedicated Nginx index

index_kibana.json: Allow Kibana to index all the correponding index to nginx-logs-*

filter_kibanajson: show logs of the namespace default in kibana


## Pre-requisite
> [!NOTE]
> - Clone the git repository from github : https://github.com/caiimy/m2i-tp5.git
> - A kubernetes cluster deployed and ready to receive deployments

# Remarque:
Ce README decrit la theorie derriere ce que j'ai fais dans ce TP, malheureusemlent j'ai pu tester que les deploiements mais pas tous le projet. 
Je fais quand meme le rendu mais je mettrais a jour le repo quand tous sera testé.