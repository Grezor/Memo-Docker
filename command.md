- ```docker ps``` liste les containers sur la machine
- ```docker images -a```
- ```docker ps -a``` , voir tout les containers meme ceux eteint
- ```docker inspect nom_container``` fournit les information nécessaire 
## container alpine

- ```docker pull [nom_image]``` pour telecharger une image
- ```docker run alpine:latest``` pour lancer, mais s'arrete ensuite
- ```docker ps -a ``` pour afficher toutes les images
- ```docker run -di --name alpine alpine:latest```
    - pour lancer un container et la renomer ici renomer alpine:lastest => alpine 
- ```docker exec -ti alpine sh``` se connecter au conteneur

## container nginx
- ```docker run -tid -p 8080:80 --name web nginx:latest```
    - lancer le container nginx sur le port 8080/80 et qui a pour nom web et ici prend la dernière version de nginx
- si l'image n'est pas telecharger, il va la telecharger
- ensuite on peux se rendre sur **127.0.0.1:8080**
- ```docker inspect web``` affiche des informations (address ip, port ..)

## volumes ngnix 
- pour lancer un container : ```docker start [nom container]```
- pour rentrer dedans: docker exec -ti web sh
pour modifier la page : ```vim /usr/share/nginx/html/index.html```
- ```docker stop web```
si par exemple je supprime mon container : ```docker rm -f web``` // -f forcer
- si on supprime le container, les datas ne reste pas


- docker run -tid -p 8080:80 -v /srv/data/ngnix/:/usr/share/nginx/html/  --name web nginx:latest
    - container avec un volumes
    - si je veux crée une page vim index.html 
    - insert du texte


# Docker volumes sur nginx : 
Docker volumes prend 5 actions, create inspect, ls, prune, rm

- pour crée un volume : docker volume create monVolume
- inpecter mon volume :  docker volume inspect monVolume
- pour reutiliser mon container : docker run -tid --name web -p 8080:80 --mount source=monVolume,target=/usr/share/nginx/html nginx:latest
- docker volume inspect monVolume
- modifier le fichier dans le Mountpoint
pour supprimer le volume: rdocker rm monVolume
    - message erreur : il faut un id
- docker rm -f web
- docker volume rm monVolume