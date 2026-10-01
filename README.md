# Projet DevOps

Ce projet met en place une stack d'infrastructure conteneurisée avec Docker Compose. Elle combine la supervision système avec Zabbix, la gestion des alertes
et l'automation de workflows via n8n, ainsi que la visualisation de données avec Grafana.

---
Groupe composé de : 
- Jacky Lefevbre
- Justine Rotge
- Nicolas Veysset

## Architecture du Projet

Le projet est découpé en 5 dossiers de builds personnalisés et orchestré par un `docker-compose.yml` définissant des réseaux isolés et des volumes persistants :

```text
ProjetDevOps/
├── docker-compose.yml  # Orchestration globale des services, réseaux et volumes
├── grafana/             # Configuration et Dockerfile pour Grafana
├── n8n/                 # Configuration et Dockerfile pour n8n
├── target-test/         # Dockerfile de la cible de test Ubuntu
├── zabbix-server/       # Configuration et Dockerfile du serveur Zabbix
└── zabbix-web/          # Configuration et Dockerfile de l'interface Web Zabbix
