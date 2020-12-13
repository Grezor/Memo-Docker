# commande docker

```bash
# Aide d'un commande 
docker <commande> --help
```
## image
```bash
# Lister les images installées
docker images
# chercher une images 
docker search <terme a chercher>
# récuperer une image
docker pull <nom de l-image>
# supprimer une image
docker rmi <nom ou id de l-image>
#crée une image a partur d'un dockerfile
docker build -t <nom de l-image> </chemin/vers/le/dockerfile/.>
```

## Conteneur
```bash
# Lister les conteneurs lancés
docker ps
# Créer un conteneur depuis une image
docker create --name <nom ou ID du conteneur> <nom de image>
# Examiner un conteneur
docker inspect <nom ou ID du container>
# Tuer un container 
docker kill <nom ou ID du container>
# Renomer un conteneur
docker rename <nom ou ID du conteneur> <nom de l-image>
# Démarrer un conteneur arrêté
docker start <nom ou ID du conteneur>
# Redémarrer un conteneur
docker restart <nom ou ID du conteneur>
```