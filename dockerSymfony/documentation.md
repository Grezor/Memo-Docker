**MYSQL_ALLOW_EMPTY_PASSWORD: ‘yes’**
l'option mysql_allow_empty_password permet d'indiquer qu'il autorise les comptes sans mot de passe
(nous somme pas en production)

**depends_on** permet au container phpmyadmin d'attendre le container mysql avant de demarrer

**restart: always** permet d'indiquer au deamon docker de redemarrer ce container en cas d'arret de celui ci
