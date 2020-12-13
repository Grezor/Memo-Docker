# Docker Prune : 

Il s'agit de deux niveaux de nettoyage de docker et des élements systèmes qui sont rattacher.

- system prune : 
    - all stopped containers
    - all networks not used by at least one container
    - all dangling images
    - all build cache 

- system prune -a : 
    - all stopped containers
    - all networks not used by at least one container
    - all volumes not used by at least one container
    - all images without at least one container associated to them
    - all build cache