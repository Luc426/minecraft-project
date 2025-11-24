# Serveur Minecraft avec Kubernetes

Déploiement d’un serveur Minecraft scalable et accessible publiquement sur une infrastructure Kubernetes.

Le serveur est entièrement conteneurisé et géré via des manifests Kubernetes, permettant un déploiement reproductible, stable et facile à maintenir.

L’accès public est sécurisé grâce à un loadbalancer MetalLB configuré pour gérer le trafic entrant, tandis que des Network Policies limitent les communications internes aux seuls services nécessaires.
Le stockage persistant assure la sauvegarde automatique du monde et des données des joueurs, même après la recréation des pods.

Ce projet met en avant l’orchestration d’un service temps réel sur Kubernetes, la gestion de la sécurité réseau, et la mise en production d’un service public à forte disponibilité.

## Liens utiles

- 🌐 [Adresse du portfolio en ligne](https://lumitek.fr)
- ☁️ [Mon Projet Cloud](https://cloud.lumitek.fr/s/tFfkts7BwxtGiBm)
- 💼 [Mon profil LinkedIn](https://www.linkedin.com/in/luclouisdelorme/)  
- 🐙 [Mon GitHub](https://github.com/Luc426)

## Contacter

**Email :** [luclouis.delorme@lumitek.fr]  

## Architecture

```bash
minecraft-project/
├── k8s
│   ├── kustomization.yaml
│   ├── network
│   │   ├── kustomization.yaml
│   │   └── networkpolicies.yaml
│   ├── statefulset
│   │   ├── kustomization.yaml
│   │   ├── service.yaml
│   │   └── statefulset.yaml
│   └── storage
│       ├── kustomization.yaml
│       ├── persistentVolumeClaim.yaml
│       └── persistentVolume.yaml
├── minecraft-app.yaml
└── README.md
```
---