# m2i-tp5

## Provided files
### Config_files
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

## Pre-requisite
- Clone the git repository from github : https://github.com/caiimy/m2i-tp5.git
- A kubernetes cluster in production

## 
Permet à Kibana d'indexer tous les index correspondant à nginx-logs-*

Affiche uniquement les logs du namespace default dans Kibana