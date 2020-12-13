## dockerfile :

le dockerfile va nous permettre d'automatiser tous ce processus.
le dockerfile sera donc le robot qui colorie les images pour nous de la couleur qu'on lui indiquera.

Finalement, le dockerfile est donc un simple fichier texte, contenant toutes les "commandes" nécessaires pour assembler l'image désirée en fonction de l'image source choisie.

voici un exemple : 
```xml
// exemple
FROM php:7.4-cli
RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
```

From // telecharge
RUN // on colorie l'image

## docker-compose 
Pour orchestrer nos conteneurs nous allons utiliser un outils qui est fourni par docker **docker compose**
