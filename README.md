# Projet *tpviz* : base de données

Dans ce dossier se trouve la base de données qui a servi dans le cadre du travail de mémoire **La couverture géographique des reportages de Temps Présent : apport des archives numériques et des visualisations de données à une histoire des magazines de grands reportages**. Ce projet porte le nom de code *tpviz*.

La base de données comporte toutes les collections qui ont servi à l'élaboration des visualisations de données. Seul, le jeux de données d'origine a été exclu pour des raisons de place. On trouve néanmoins dans la db une collection intitulée *tp_show_lite* qui comporte une version allégée du dataset original qui décrit les reportages de *Temps Présent*. Pour plus de détails sur la méthode d'aquisition du jeux de données voir chapitre 2 du mémoire.

L'obtention du dataset d'origine est possible via l'interface https://developer.srgssr.ch/apis/rts-archives-v3

l'identifiant de l'émission *Temps Présent* est le 103. J'ai créé une librairie Python qui permet de faire facilement des requêtes sur cette interface : https://github.com/rerouj/ssr_rts_api

## Comment ?

A l'origine la base de données a été créée sur un système Mongodb shell version v4.2.3. Pour installer cette db, il faut :

1. Télécharger et ouvrir le fichier apptp-db.zip dans un dossier local
2. Installer Mongodb shell localement
3. Créer une db vide intitulée *apptp-db* dans Mongodb avec la commande *use* : 
```javascript
use apptp-db
```
3. Mobiliser la fonctionalité mongorestore (en ligne de commande et en dehors du shell mongodb) pour *dumper* les collections dans la db. documentation : https://docs.mongodb.com/database-tools/mongorestore/#bin.mongorestore

## Qui ?

Hormis la collection *tp_show_lite*, les collections ont toutes été produite par l'auteur du mémoire (Renato Diaz). Les technologies mobilisées pour produire les différents jeux de données est Python. La méthode est détaillée dans le dossier Github https://github.com/rerouj/apptp-data-engine et dans le chapitre 4 du mémoire.

contact : renato.diaz@outlook.com