```ini
# Aide d'un commande 
docker <commande> --help
```
## image
```ini
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
```shell
# lister les conteneurs lancés
docker ps
# créer un conteneur depuis une image
docker create --name <nom ou ID du conteneur> <nom de image>

```