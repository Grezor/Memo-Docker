- docker run hello-world
- l'image ce telecharge

- Demarrer un server Ngnix avec un container docker 
```
docker run -d -p 8080:80 nginx

-d // détacher le container
-p //pour définir le port, ici port 8080 vers le port 80 du conteneur
ensuite ce rendre http://127.0.0.1:8080
```

pour arreter un container : docker stop 