## Semaine 1
Présentation de Pix(le robot) et premières configurations

Problèmes d'initialisation du LeJOS, besoin d'un JDK 1.7, les versions d'éclipse depuis 2025 utilisent à minima un JDK 1.8

## Semaine 2
Configuration terminée, lancement de petits programmes pour tester


**Observations :**
- Pix a peut etre une vitesse max: autour de 700 (on va dire 700up [unités de Pix]) ou moins. En gros pour les deux grands moteurs B et C il est inutile d'augmenter la vitesse au-delà de 700, c'est faisable en pratique mais même en mettant 32000, les moteurs iront à un maximum de 700.
- Une seule roue fonctionne lors de la rotation ??
- Soucis pour fermer la pince au max: résolu la vitesse du petit moteur a une plus grosse limite que celle du grand moteur ( elle n'est pas limitée à 700, cependant, la limite est difficile à estimer.

**A noter :**
  Affichage du nom du robot réussi.

## Semaine 3
Centralisation des documents internes présents sur les autres branches dans le main :
branches "cahier-des-charges" et "cahier-de-bord" (supprimées suite au regroupement).

**Observations du jour** : 
- angle de rotation de PIX: tour complet: angle 840° (en degrés de PIX ),
- La deuxième roue était branchée sur le mauvais moteur, tout est réaligné
- Le tachymètre marche en ouverture mais pas en fermeture, les angles renvoyés sont différents, résultats du tachymètre inutilisable pour les pinces.

- découverte de nouvelles stratégies pour récupérer au plus vite les premiers palets, particulièrement le premier (mise en place d'un circuit prédéfini pour les premiers palets)
- capteurs ultrasons: fonctionne et renvoie une série de valeur
- capteur lumière: reconnait les couleurs du terrain (rouge, jaune, vert, blanc, noir, bleu)
- les pinces: problème de fermeture (pour l'instant)
- modification de Github (réorganisation des dossiers)
- on estime que PIX parcours 55.5 cm en 1 seconde (mesure imprécise, la vitesse de PIX est mesuré en (°/s)il faudra effectuer de nouvelle mesure et convertir pour obtenir des (cm/s)(La formule de conversion est :Vitesse(cm/s)=Vitesse angulaire(°/s)*(pi/180)*Rayon(cm))).
- 1ère réussite de saisie de palet de PIX , on observe cependant des complications(vélocité mal géré et interprété , décalage par rapport à un axe donné du aux frottements des roues) lorsque l'on essaye à plus grande vitesse aussi bien pour les pinces que pour les roues.

## Semaine 4
- Diamètre d'une roue = 55 mm
- Vitesse max estimée de PIX ≃33.5975881 cm/s
- Ouverture et fermeture des pinces : opérationnel
- PIX peut attraper un palet et avancer avec
- Remise en forme des fonctionnalités du cahier des charges (détails avec Tanis)
- Test du capteur ultrasons avec retour d'une seule valeur mesuré à un instant t
- Dépot de la première version du plan de développement
- Retrait de la toute première version du cahier des charges(il ne servait plus à rien)

## Semaine 5
- Modification du plan de développement (ajout des taches modulaire, pour fixer une estimation temporelle plus efficacement)
-  Définition de méthode pour récupérer les valeurs renvoyés par le capteur ultrason
-  Révision quant à la définition du capteur couleur, voir avec Ekoumi(passage de colorId à getmodeRGB)
-  Passage à la classe pilot pour les mouvements

## Semaine 6
- Tests du capteurs ultrason
- Détection des palets en effectuant un 360

## Semaine 7
- Tests concluants des tâches suivantes : Relâcher le palet dans la zone de départ(à revoir car méthode reconnaissance couleur inachevé), Déclencher une alerte si la distance mesurée est < Xcm.
- Après discussion, changement de méthode pour détecter les palets : nous optons pour une méthode plus efficace et beaucoup plus rapide.
- Nouvelles stratégies pour la course
- Prise en considération des méthodes à coder pour ces nouvelles stratégies (déplacement, utilisation des données)


## Semaine 8
- méthode d'identification couleur pas utile d'apres prof alternative: utiliser l'exploitation des données pendant un tour complet pour détecter un palet et calculer l'angle en fonction du nombre de données pour se retrouver devant le palet
- caméra zénithale à revoir
- rajout de deux nouvelles taches 
